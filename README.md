Test-Driven Development
=======================


<img src="https://avatars.githubusercontent.com/u/46154?v=4" width="32px"
/> [Canonical TDD](https://tidyfirst.substack.com/p/canon-tdd) ([Kent Beck](https://en.wikipedia.org/wiki/Kent_Beck))
------------------

**OBJECTIVES:**
* Everything that used to work still works.
* The new behavior works as expected.
* The system is ready for the next change.
* The programmer & their colleagues feel confident in the above points.

**STEPS:**
1. Write a list of the test scenarios you want to cover.
2. Turn exactly one item on the list into an actual, concrete, runnable test.
   - **3A** (Bill Wake):
     |    |           |                      |
     |:--:|-----------|----------------------|
     | 1. | _Arrange_ | Create some objects. |
     | 2. | _Act_     | Stimulate them.      |
     | 3. | _Assert_  | Check the results.   |
     
4. Change the code to make the test (& all previous tests) pass (adding items to the list as you discover them).
5. Optionally refactor to improve the implementation design.
6. Until the list is empty, go back to #2.


<a href="https://github.com/unclebob"><img src="https://avatars.githubusercontent.com/u/36901?v=4" width="32px"
/></a> [Three Laws of TDD](http://www.butunclebob.com/ArticleS.UncleBob.TheThreeRulesOfTdd) [<img src="https://user-images.githubusercontent.com/7102064/160022421-ed9425eb-6a6b-4849-a090-5a27542b60c3.png" width="16px" />](https://youtu.be/qkblc5WRn-U) ([Uncle Bob](https://en.wikipedia.org/wiki/Robert_C._Martin))
-------------------

* _**Rule 1:**_ You are not allowed to write any production code unless it is to make a failing test pass.
* _**Rule 2:**_ You are not allowed to write anymore of a unit test than is sufficient to fail; and compilation failures are failures.
* _**Rule 3:**_ You are not allowed to write anymore production code than is sufficient to pass the one failing unit test.


<img src="https://www.wikipedia.org/portal/wikipedia.org/assets/img/Wikipedia-logo-v2.png" width="32px"
/> [Development Cycle](https://en.wikipedia.org/wiki/Test-driven_development#Test-driven_development_cycle) (Wikipedia)
-------------------

01. **Add a small / incremental test** for a new feature by discovering specifications from [user stories](https://en.wikipedia.org/wiki/User_story) / [use cases](https://en.wikipedia.org/wiki/Use_case) / [requirements](https://en.wikipedia.org/wiki/Requirement).
02. **Run all tests** to verify the new test actually fails, for expected reasons, and that new code is actually needed.
03. **Write the simplest code that passes the new test** and nothing more, even if it's inelegant or hard coded.
04. **All tests should now pass** or else revise the new code, until they do, to ensure new code meets test's requirements and doesn't cause [regressions](https://en.wikipedia.org/wiki/Software_regression) (ie. break existing features).
05. **[Refactor](https://en.wikipedia.org/wiki/Code_refactoring), for readablility / maintainability, while running tests to ensure functionality is preserved**
    - Move code to where it logically belongs.
    - Remove [hard-coded](https://en.wikipedia.org/wiki/Hard_coding) test data.
    - Remove [duplicate code](https://en.wikipedia.org/wiki/Duplicate_code).
    - Make names [self-documenting](https://en.wikipedia.org/wiki/Self-documenting_code).
    - Split methods into smaller pieces.
    - Re-arrange inheritance hierarchies.
06. **Repeat** cycle for each new piece of functionality.

_*Commit often and undo / revert new code which fails any tests, rather than debugging excessively._


<a href="https://github.com/jitterted"><img src="https://avatars.githubusercontent.com/u/47930468?s=200&v=4" width="32px"
/></a> [Clarify Goals](https://ted.dev/articles/2021/03/05/clarifying-the-goal-of-behavior-change/) [<img src="https://user-images.githubusercontent.com/7102064/160022421-ed9425eb-6a6b-4849-a090-5a27542b60c3.png" width="16px" />](https://youtu.be/P8eRY2c8NFY) ([JitterTed](https://github.com/jitterted))
---------------

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


💡 More Info
------------

* [Structure and Interpretation of Test Cases](https://youtu.be/MWsk1h8pv2Q) - Kevlin Henney (youtube video)
* [Use Cases are Essential](https://dl.acm.org/doi/pdf/10.1145/3631182) - Ivar Jacobson & Alistair Cockburn
* [IntegrationTest](https://martinfowler.com/bliki/IntegrationTest.html) - Martin Fowler
* [XP Design Rules](https://martinfowler.com/bliki/BeckDesignRules.html) - Martin Fowler
* [Focus on Branch Logic](https://www.geepawhill.org/2019/02/18/pro-tip-tdd-focus-on-our-branching-logic/) - GeePaw
* Assertions: [Java](https://docs.oracle.com/javase/8/docs/technotes/guides/language/assert.html); [Python](https://wiki.python.org/moin/UsingAssertionsEffectively)
* [Glossary of Software Testing Terms](https://astqb.org/assets/documents/Glossary-of-Software-Testing-Terms-v3.pdf) - ISTQB
* Refactoring to Design Patterns: [preface](https://courses.cs.duke.edu/compsci308/spring24/readings/kerievsky_preface.pdf); [catalog](https://www.industriallogic.com/refactoring-to-patterns/catalog/)


:octocat: Version Control
-------------------------

[Git](https://git-scm.com/docs/gittutorial)

```
git init .
git add .
git status
git commit -m "Commit message"
git log [--oneline] [--author=name]
git tag 1.0.0 <commit-id-from-log>

git restore --staged <file>
git restore <file>
git reset --hard

git stash
git stash pop

git checkout -b <new_feature_branch_name>
git diff [--cached]
git checkout <master | main>
git branch
git merge --squash <new_feature_branch_name>
git branch --delete <new_feature_branch_name>

git clone [--no-single-branch] git@github.com:veganaiZe/TDD.git
git clone [--depth=50] https://github.com/veganaiZe/TDD.git
git remote add origin <original_upsteam_repo_server>
git pull --rebase
git push
```

✏️ Personal Notes
-----------------

* Constantly check/consider code against design principles:
  - [KISS](https://en.wikipedia.org/wiki/KISS_principle): keep it short & simple; do the simplest thing that could possibly work, first.
  - [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself): don't repeat yourself (more than a very few times).
  - [POLA](https://en.wikipedia.org/wiki/Principle_of_least_astonishment): principle of least astonishment.
  - [YAGNI](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it): you ain't gonna need it.
  - _"Never let perfect be the enemy of good enough." (for now)_
  - _"As little as possible; As much as necessary."_
  - [SOLID](https://en.wikipedia.org/wiki/SOLID):
    - [SRP](https://en.wikipedia.org/wiki/Single-responsibility_principle): single responsibility principle; do one thing well.
    - [OCP](https://en.wikipedia.org/wiki/Open%E2%80%93closed_principle): open-closed principle; extend, don't modify.
    - [LSP](https://en.wikipedia.org/wiki/Liskov_substitution_principle): liskov substitution principle; subtype like basetype.
    - [ISP](https://en.wikipedia.org/wiki/Interface_segregation_principle): interface segregation principle; granular interfaces.
    - [DIP](https://en.wikipedia.org/wiki/Dependency_inversion_principle): dependency inversion principle; inject dependencies.

* When on the fence over whether or not to pre-process data, or process it at runtime, write/tdd the common functionality before deciding.
* The `main` function is not TDDed; The application's `main` code is replaced by the unit tests' `main` code, and vice versa; The application's `main` code is tested at the user interface level (top) of the [test pyramid](https://en.wikipedia.org/wiki/Test_automation#Testing_at_different_levels).
