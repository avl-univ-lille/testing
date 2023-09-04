# Mutation testing practice

In this practice, we will learn how to use mutation testing on a real project to evaluate test quality.
For this purpose, we will use the [mutalk](https://github.com/pharo-contributions/mutalk) library on top of Pharo 11.

## Setup

For this practice, you will need to:
 - install the pharo launcher
 - install Pharo11 through the launcher
 - install mutalk in Pharo:
   - open a playground
   - execute the following expression:
  
```smalltalk
Metacello new
  baseline: 'MuTalk';
  repository: 'github://pharo-contributions/mutalk/src';
  load.
```

## Warming-up with UUID

Evaluate the quality of Pharo's UUID library:

```smalltalk
testCases :=  { UUIDPrimitivesTest }.
classesToMutate := { UUID . UUIDGenerator }.

analysis := MutationTestingAnalysis
    testCasesFrom: testCases
    mutating: classesToMutate
    using: MutantOperator contents
    with: AllTestsMethodsRunningMutantEvaluationStrategy new.

analysis run.
```

Executing the previous code does have some interesting outcomes.
First, we can ask ther result for the mutation score. In this case, we have a score of 69, meaning that 69% of the mutants were killed.

```smalltalk
analysis generalResult mutationScore
```

Also, we can retrieve the alive mutants to work on them programatically.
Doing programatic analysis being a bit more hardcore for a first approach, we will better do it through a GUI instead in next section.

```smalltalk
"To retrieve the alive mutations"
alive := analysis generalResult aliveMutants.
```

### Understanding alive mutants

Inspecting the `generalResult` object yields a GUI showing the surviving mutants.
We can now click on them, see what is the code that was changed and do a case-by-case analysis to see what happened.

```smalltalk
analysis generalResult.
```

<img width="883" alt="imagen" src="https://github.com/avl-univ-lille/testing/assets/708322/af19408c-07cb-4412-9efa-e0d3cef5e230">

Remember, when a mutant remains alive this means that no test broke due to this change.
This could be due to many different issues. Either
 - the test suite is not strong enough: we miss some tests
 - the mutation is equivalent: the code mutated but generated code that does the same
 - or (as a special case of the previous one) the mutated code is dead code: thus it will never be executed

### Increasing the mutation score

The best way to increase the mutation score is to write a test covering the missing case.
Fortunately, there are more tests for UUID in the `UUIDTest` class.

1. Change the list of test classes from

```smalltalk
testCases :=  { UUIDPrimitivesTest }.
```

to:

```smalltalk
testCases :=  { UUIDPrimitivesTest. UUIDTest }.
```

2. Run the analisys again. What is the different in score now?


Now that we have harvested the low-hanging fruits, we can try to write a test.
For example, we see lots of mutations survived in the following method:

```
UUID >> < aMagnitude
	"Answer whether the receiver is less than the argument."

	self size = aMagnitude size ifFalse: [ ^ self size < aMagnitude size ].
	1 to: self size do: [ :i |
		(self at: i) = (aMagnitude at: i) ifFalse: [
			^ (self at: i) < (aMagnitude at: i) ] ].
	^ false
```

This means that method is probably not covered at all.
If we check the class `UUIDTest` we will find the following method:

```smalltalk
UUIDTest >> testComparison
	| a b |
	a := UUID fromString: '0608b9dc-02e4-4dd0-9f8a-ea45160df641'.
	b := UUID fromString: 'e85ae7ba-3ca3-4bae-9f62-cc2ce51c525e'.

	self assert: a equals: a copy.
	self assert: a <= a copy.
	self assert: a >= a copy.
	self assert: b equals: b copy.
	self assert: b <= b copy.
	self assert: b >= b copy.
	self assert: a < b.
	self assert: a <= b.
	self assert: b > a.
	self assert: b >= a.

	self deny: a > b equals: b > a.
	self deny: a >= b equals: b >= a
```

Something not very obvious because this test is long, is that we are never comparing `a < a`!
Thus, we never compare two uuids that are equal.
In the same vein, we never compare `b < a`.

3. add those cases in our test, run the analysis again and explore the results.

4. Extend the list of test classes to also include `UUIDGeneratorTest`, run the analysis again and analyse the survivors.
   - which ones look like equivalent mutants? why?
   - can you change the method `UUIDGenerator>>#nextRandom16` to increase the coverage even further?
