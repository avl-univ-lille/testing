# AVL - Testing

## Organisation

- Week 1: Testing 101 + Test Desing
  - make your teams
  - choose a paper, start reading
  - choose a project topic, start coding
- Week 2: Automatic Test Generation
- Week 3: Extreme TDD
  - presentations

[Discord server](https://discord.gg/h2mH5Daq)

Idea: Split work in your team! Some doing research, some doing implementation. Communicate often between you (discord?). Make a log of what you are doing and the state of the project(s).

## Research Paper Presentations

What is expected? a 15' presentation. Each team member should speak. Each should answer one question.
When is the deadline? The prepsentation will take place the 3rd week.

Choose one of the following:
 - [QuickCheck - Property Based Testing](https://www.cs.tufts.edu/~nr/cs257/archive/john-hughes/quick.pdf) 
 - [DART - Concolic Testing](https://web.eecs.umich.edu/~weimerw/590/reading/p213-godefroid.pdf)
 - [Mutation Testing](https://edisciplinas.usp.br/pluginfile.php/1943431/mod_resource/content/1/Hints_on_Test_Data_Selection-Demillo.pdf)
 - [Delta Debugging - test case reduction](https://www.cs.purdue.edu/homes/xyzhang/fall07/Papers/delta-debugging.pdf)
 - [Test Case Selection](https://hal.inria.fr/hal-01344842/document)
 - [Rotten Green tests](https://hal.inria.fr/hal-02002346v2/document)
 - [Differential testing](https://www.cs.swarthmore.edu/~bylvisa1/cs97/f13/Papers/DifferentialTestingForSoftware.pdf)
 
### Some hints to read a scientific paper
  - read first abstract, intro and conclusion. Try to get what the paper is about.
  - Try to understand what the problem is before diving into the details. Look for examples.
  - If you understand the problem, you can move on either to
    - implementation (if you want to replicate it)
    - evaluation/results to see how the solution works out in practice

## Project Ideas

### What is expected?
Implement a simple project. For example, a simple TODO list, or a grocery list using one of:
 - a sql database (e.g., SQLite)
 - a GUI (e.g., vue.js, react.js...)
 - an object serialiser (CVS, JSON,...) - for the purpose of the exercise, try writing your own JSON/CVS serialiser or parser!

Deliverables:
 - a git repository with the code
 - code should be loadable and runnable with a script
 - a **README file** should explain how to install it and run it
 - a **report** written in markdown should be available in the same repository explaining
   - what testing decisions you took
   - what was tested and why
   - did you use some advanced technique? what? where? why?

Restrictions:
 - Use one of the following programming languages: Pharo, Python, C

### When is the deadline? The end of the trimester (at the end of the sixth week)
 
### Some hints for the project
- The project will be graded based on testing, not project features!
- Thus, make few features, but interesting from the testing point of view (with more cases to test)
- write some hand written tests and try to find some libraries that already do advanced testing stuff!
