Test-Driven Development
=======================


Three Laws of TDD ([Uncle Bob <img src="https://user-images.githubusercontent.com/7102064/160022421-ed9425eb-6a6b-4849-a090-5a27542b60c3.png" width="16px" />](https://youtu.be/qkblc5WRn-U))
-----------------

* _**Rule 1:**_ You are not allowed to write any production code unless it is to make a failing test pass.
* _**Rule 2:**_ You are not allowed to write anymore of a unit test than is sufficient to fail; and compilation failures are failures.
* _**Rule 3:**_ You are not allowed to write anymore production code than is sufficient to pass the one failing unit test.


Development Cycle ([Wikipedia](https://en.wikipedia.org/wiki/Test-driven_development#Test-driven_development_cycle) / Kent Beck)
-----------------

01. **Add a small / incremental test** for a new feature by discovering specifications from user stories / use cases / requirements.
02. **Run all tests** to verify the new test actually fails, for expected reasons, and that new code is actually needed.
03. **Write the simplest code that passes the new test** and nothing more, even if it's inelegant or hard coded.
04. **All tests should now pass** or else revise the new code, until they do, to ensure new code meets test's requirements and doesn't cause regressions (ie. break existing features).
05. **Refactor, for readablility / maintainability, while running tests to ensure functionality is preserved**
    - Move code to where it logically belongs.
    - Remove hard-coded test data.
    - Remove duplicate code.
    - Make names self-documenting.
    - Split methods into smaller pieces.
    - Re-arrange inheritance hierarchies.
06. **Repeat** cycle for each new piece of functionality.

_*Commit often and undo / revert new code which fails any tests, rather than debugging excessively._


Improved Cycle ([Jitterted](https://ted.dev/articles/2021/03/05/clarifying-the-goal-of-behavior-change/))
--------------

01. What should it do? (verbalize the goal; be clear & precise)
02. How will you know it did it? (expected outcome; observable)
03. Write test for code yet-to-be.
04. (Fails to compile.)
05. Write least amount of code to compile.
06. Predict how test will fail. (hypothesize)
07. Run test.
08. (Fails in predicted way.)
09. Write least amount of code to pass.
10. Predict it will pass.
11. Run test.
12. (Passes!)


More Info
---------

* [Focus on Branch Logic](https://www.geepawhill.org/2019/02/18/pro-tip-tdd-focus-on-our-branching-logic/) - GeePaw
* Assertions: [Java](https://docs.oracle.com/javase/8/docs/technotes/guides/language/assert.html); [Python](https://docs.python.org/3/reference/simple_stmts.html#the-assert-statement)
