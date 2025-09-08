# Agenda

| Week   | Before Break | After Break | Extras |
|--------|--------------|-------------|--------|
| 1 - 08/09      | Modules 0, 1 + Kata together | Kata in teams  | -
| 2 - 15/09 | Module 2 | Mutation Practice | Mini Exam testing
| 3 - 22/09 | Modules 3, 4 | Fuzzing Practice | Mini Exam mutations
| 4 - 29/09 | Module 5 | TP | -
| 5 - 06/10 | Module 6 | Constant Propagation | TP
| 6 - 13/10 | Presentations | Presentations | Second chances and Oral exam if needed

# Details

Most resources are in the slides.
Find below extra links that may be useful.

## Resources Week 1

- **Kata together:** https://github.com/garora/TDD-Katas/tree/main/src#yehtzee-
- **Kata in teams:** https://github.com/gigasquid/wonderland-clojure-katas/tree/master/tiny-maze
- **More Katas:** https://github.com/gamontal/awesome-katas?tab=readme-ov-file

- **Quick Intro Pharo:** https://github.com/avl-univ-lille/testing/blob/2024/practice/0-pharo-introduction.md
- **Intro Pharo Videos:** https://advanced-design-mooc.pharo.org/#module0
- **Setting up Pharo:** https://github.com/avl-univ-lille/testing/blob/2024/practice/0-setup-pharo.md

- **Refreshing OOP:** https://advanced-design-mooc.pharo.org/#module1
- **Mooc Testing:** https://advanced-design-mooc.pharo.org/#module2

- **Testing Strategies Scenarios:** https://github.com/avl-univ-lille/testing/blob/2024/practice/optional-testing-strategies.pdf

## Resources Week 2

- **Mutation analysis practice:** https://github.com/avl-univ-lille/testing/blob/2024/practice/1-mutation.md

## Resources Week 3

- **Fuzzing intro and practice:** https://github.com/avl-univ-lille/testing/blob/2024/practice/2-fuzzing.md
- **Differential Testing:** https://github.com/avl-univ-lille/testing/blob/2024/practice/3-differential-testing.md
- **Mutation Fuzzing:** https://github.com/avl-univ-lille/testing/blob/2024/practice/4-mutation-fuzzing.#md

# TP: Analysis of a property-based testing framework

For the TP and final grade, you will do a presentation in teams about a property-based testing framework of your choice.

1. Split in teams
2. Choose a property-based testing library/framework of your liking
3. Perform and analysis:
  - how do they solve fuzzing?
  - what kind of oracles/properties do they support?
  - Do they solve issues related to dynamic-typing and polymorphism?
  - How is the framework extended with new kind of features/properties/fuzzers?
4. Ideally, find and study a research paper talking about it

The task: Prepare a 30' presentation for the last week
  - Explain how the framework works and how is it used
  - Show examples
  - Show implementation details

Tips: 
  - Execute the code! Write examples yourselves! *Be curious.*
  - Dive inside the code to find interesting design decisions, and see how they solved their problems in practice.
