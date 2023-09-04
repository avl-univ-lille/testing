# Analyse et Verification des Logiciels - Testing

This repository contains the material of a (short) advanced testing course originally developed for the Master 2 Génie Logiciel @ Université de Lille.

- [Course Agenda](agenda.md)
- [Course Material](slides)
- [Course Practices](practice)
- [TP/Homework](tp.md)

Get in contact!
- [Discord server](https://discord.gg/h2mH5Daq)
- email: guillermo.polito_at_inria.fr


## Modules

- **Module 0: Testing Refresher.** Importance of testing. RIGHT BICEP principle: Right, boundaries, inverse and error conditions, cross-checks, and performance. Automated testing. Unit testing frameworks. Examples: JUnit and SUnit.
- **Module 1: Mutation Analysis.** Computing test case quality as the ability to detect bugs. Competent developer hypothesis. Simulating developer errors with artificial mutations. Mutation operators, mutations, mutants. Killed and surviving mutants. Mutation score. Equivalent mutants and trivial mutants.
- **Module 2: Introduction to Fuzzing.** Testing with randomly generated data. Fuzzing. Guide fuzzers with domain knowledge. Building an initial fuzzing framework. Evaluating results.
- **Module 3: Grammar-Based Fuzzing.** Compilers Phases as fuzzing barriers. Syntactic fuzzing based on grammars. Building a Grammar fuzzer.
- **Module 4: The Oracle Problem.** The Oracle problem. Derived, specified, and implicit oracles. Dealing with the absence of oracles. Introducing the Oracle problem for compilers.
- **Module 5: Differential Testing.** Comparing existing systems to evaluate behavior. Dealing with the absence of ground truth.

## Bibliography

- A. Zeller, R. Gopinath, M. Böhme, G. Fraser and C. Holler. (2021). The Fuzzing Book.
CISPA Helmholtz Center for Information Security. https://www.fuzzingbook.org/. Retrieved
2021-10-26 21:30:20+08:00.
- Barr, E. T., Harman, M., McMinn, P., Shahbaz, M., & Yoo, S. (2014). The oracle problem in
software testing: A survey. IEEE transactions on software engineering, 41(5), 507-525.
- McKeeman, W. M. (1998). Differential testing for software. Digital Technical Journal, 10(1),
100-107.
- DeMillo, R. A., Lipton, R. J., & Sayward, F. G. (1978). Hints on test data selection: Help for
the practicing programmer. Computer, 11(4), 34-41.

## Bibliography -- extra

- Claessen, K., & Hughes, J. (2000, September). QuickCheck: a lightweight tool for random
testing of Haskell programs. In Proceedings of the fifth ACM SIGPLAN international
conference on Functional programming (pp. 268-279).
- Chen, T. Y., Cheung, S. C., & Yiu, S. M. (2020). Metamorphic testing: a new approach for
generating next test cases. arXiv preprint arXiv:2002.12543.
- Polito, G., Tesone, P., Ducasse, S., Fabresse, L., Rogliano, T., Misse-Chanabier, P., &
Hernandez Phillips, C. (2021, September). Cross-ISA testing of the Pharo VM: lessons
learned while porting to ARMv8. In Proceedings of the 18th ACM SIGPLAN International
Conference on Managed Programming Languages and Runtimes (pp. 16-25).
- Godefroid, P., Kiezun, A., & Levin, M. Y. (2008, June). Grammar-based whitebox fuzzing. In
Proceedings of the 29th ACM SIGPLAN conference on programming language design and
implementation (pp. 206-215).
- Godefroid, P., Klarlund, N., & Sen, K. (2005, June). DART: Directed automated random
testing. In Proceedings of the 2005 ACM SIGPLAN conference on Programming language
design and implementation (pp. 213-223).
- Polito, G., Ducasse, S., & Tesone, P. (2022, June). Interpreter-guided differential JIT
compiler unit testing. In Proceedings of the 43rd ACM SIGPLAN International Conference on
Programming Language Design and Implementation (pp. 981-992).
- Fraser, G., & Zeller, A. (2010, July). Mutation-driven generation of unit tests and oracles. In
Proceedings of the 19th international symposium on Software testing and analysis (pp.
147-158).
- Converse, H., Olivo, O., & Khurshid, S. (2017, March). Non-semantics-preserving
transformations for higher-coverage test generation using symbolic execution. In 2017 IEEE
International Conference on Software Testing, Verification and Validation (ICST) (pp.
241-252). IEEE.
- Nagy, S., & Hicks, M. (2019, May). Full-speed fuzzing: Reducing fuzzing overhead through
coverage-guided tracing. In 2019 IEEE Symposium on Security and Privacy (SP) (pp.
787-802). IEEE
