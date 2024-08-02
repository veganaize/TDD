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
06. Predict how test will fail. (precisely)
07. Run test.
08. (Fails in predicted way.)
09. Write least amount of code to pass.
10. Predict it will pass.
11. Run test.
12. (Passes!)


💡 More Info
------------

* [Dispelling Myths About TDD](https://www.agileinstitute.com/articles/dispelling-myths-about-test-driven-development) - Agile Institute
* [How to debug small programs](https://ericlippert.com/2014/03/05/how-to-debug-small-programs/) - Eric Lippert
* [What's in a Story?](https://dannorth.net/whats-in-a-story/) - Dan North
* [Introducing BDD](https://dannorth.net/introducing-bdd/) - Dan North
* [Spike Solutions](https://www.jamesshore.com/v2/books/aoad1/spike_solutions) - James Shore
  - [Spikes in Scrum: The Exception, not the Rule](https://web.archive.org/web/20180712125321id_/https://scrumalliance.org/learn-about-scrum/agile-atlas/agile-atlas-commentaries/may-2014/spikes-in-scrum-the-exception,-not-the-rule) - Scrum Alliance
* [Structure and Interpretation of Test Cases](https://youtu.be/MWsk1h8pv2Q) - Kevlin Henney (youtube video)
* [Unit Testing Best Practices](https://learn.microsoft.com/en-us/dotnet/core/testing/unit-testing-best-practices) - Microsoft
* [Use Cases are Essential](https://dl.acm.org/doi/pdf/10.1145/3631182) - Ivar Jacobson & Alistair Cockburn
* [IntegrationTest](https://martinfowler.com/bliki/IntegrationTest.html) - Martin Fowler
* [XP Design Rules](https://martinfowler.com/bliki/BeckDesignRules.html) - Martin Fowler
* [Focus on Branch Logic](https://www.geepawhill.org/2019/02/18/pro-tip-tdd-focus-on-our-branching-logic/) - GeePaw
* Assertions: [Java](https://docs.oracle.com/javase/8/docs/technotes/guides/language/assert.html); [Python](https://wiki.python.org/moin/UsingAssertionsEffectively)
* [Glossary of Software Testing Terms](https://astqb.org/assets/documents/Glossary-of-Software-Testing-Terms-v3.pdf) - ISTQB
* [Cost of Poor Quality Software](http://web.archive.org/web/20200817233131id_/https://www.it-cisq.org/the-cost-of-poor-quality-software-in-the-us-a-2018-report/The-Cost-of-Poor-Quality-Software-in-the-US-2018-Report.pdf) - CISQ
* Refactoring to Design Patterns: [preface](https://courses.cs.duke.edu/compsci308/spring24/readings/kerievsky_preface.pdf); [catalog](https://www.industriallogic.com/refactoring-to-patterns/catalog/)
* Wikipedia
  - [Acceptance Testing](https://en.wikipedia.org/wiki/Acceptance_testing)
  - [Anti-Pattern](https://en.wikipedia.org/wiki/Anti-pattern)
  - [Extreme Programminng](https://en.wikipedia.org/wiki/Extreme_programming)
    - [extremeprogramming.org](http://www.extremeprogramming.org/) <img src="http://www.extremeprogramming.org/images/xplinksm.gif" width="29px" />
  - [Functional Testing](https://en.wikipedia.org/wiki/Functional_testing)
  - [Fuzz Testing](https://en.wikipedia.org/wiki/Fuzzing)
  - [Integration Testing](https://en.wikipedia.org/wiki/Integration_testing)
  - [Side Effect](https://en.wikipedia.org/wiki/Side_effect_(computer_science))
  - [Usability Testing](https://en.wikipedia.org/wiki/Usability_testing)
* [Scrum Guide](https://scrumguides.org/) (official)
  - [Changed Words in Scrum Guide 2020](https://www.scrum.org/resources/blog/words-changed-scrum-guide-2020-update)
  - [Removed Words in Scrum Guide 2020](https://www.scrum.org/resources/blog/scrum-guide-2020-update-what-has-been-removed)
  - [2017 Scrum Guide](https://scrumguides.org/docs/scrumguide/v2017/2017-Scrum-Guide-US.pdf) (old)


:octocat: Version Control
-------------------------

[Git](https://git-scm.com/docs/gittutorial); [Signing Your Work](https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work); [Better Commit Messages](https://www.freecodecamp.org/news/how-to-write-better-git-commit-messages/); [Git Aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases)  
[Github Flow](https://docs.github.com/en/get-started/using-github/github-flow); [Gitflow - Vincent Driessen's branching model](https://nvie.com/posts/a-successful-git-branching-model/)  
[Github Markdown](https://docs.github.com/en/get-started/writing-on-github); [Stackoverflow Markdown](https://stackoverflow.com/editing-help); [Github Task Lists](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/about-task-lists)
<pre>
git [command] -h      # Help in console
git &lt;command> --help  # As man page (Linux); in browser (Windows)
git init .
git add .
git add -u  # stage tracked (modified & deleted) files only
git status
git commit -m "Commit message"
git log [--oneline] [--author=name]
git tag 1.0.0 &lt;commit-id-from-log>

git restore --staged &lt;file>
git restore &lt;file>
git reset --hard

git <a href="https://git-scm.com/book/en/v2/Git-Tools-Stashing-and-Cleaning">stash</a> [-u | --include-untracked]
git stash list
git stash branch &lt;new_branchname>
git stash pop

git checkout -b &lt;new_feature_branch_name>
git diff [--cached]
git checkout &lt;master | main>
git branch  # List branches; Highlight current
git merge --squash &lt;new_feature_branch_name>
git branch [-d | --delete | -D] &lt;new_feature_branch_name>

git clone [--no-single-branch] git@github.com:veganaiZe/TDD.git
git clone [--depth=50] https://github.com/veganaiZe/TDD.git
git <a href="https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes">remote</a> add origin &lt;original_upsteam_repo_server>
git pull --rebase
git push
</pre>


✏️ Personal Notes
-----------------

* Constantly check/consider code against design principles:
  - [KISS](https://en.wikipedia.org/wiki/KISS_principle): ***keep it short & simple***; do the simplest thing that could possibly work, first.
  - [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself): ***don't repeat yourself*** (more than a very few times -- ie. ***get WET first!***).
  - [POLA](https://en.wikipedia.org/wiki/Principle_of_least_astonishment): ***principle of least astonishment*** --measured by f-words per minute.
  - [YAGNI](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it): ***you ain't gonna need it***.
  - ***"Never let perfect be the enemy of good enough." (for now)***
  - ***"As little as possible; As much as necessary."***
  - [SOLID](https://en.wikipedia.org/wiki/SOLID):
    - [SRP](https://en.wikipedia.org/wiki/Single-responsibility_principle): single responsibility principle; ***do one thing well.***
    - [OCP](https://en.wikipedia.org/wiki/Open%E2%80%93closed_principle): open-closed principle; ***extend, don't modify.***
    - [LSP](https://en.wikipedia.org/wiki/Liskov_substitution_principle): liskov substitution principle; ***subtype like basetype.***
    - [ISP](https://en.wikipedia.org/wiki/Interface_segregation_principle): interface segregation principle; ***granular interfaces.***
    - [DIP](https://en.wikipedia.org/wiki/Dependency_inversion_principle): dependency inversion principle; ***inject dependencies.***


<img src="https://github.com/user-attachments/assets/20044412-0611-4bb9-ad6f-8c50435753e3" width="32px"
/> veganaiZe's TDD Steps
------------------------

1. Determine the next desired method/interface: from the perspective of the application's code.
2. Create a new development branch, and switch to it: `git checkout -b new-branch-name`
3. Write just enough __*TEST CODE*__, for a desired interface (in "Act" section), to observe the __*TEST FAILING*__ against the application's missing interface code.
4. Write just enough __*APPLICATION CODE*__, implementing an empty method (returning the correct type), to observe the __*TEST PASSING*__ against the application's *incorrect* return value.
5. Write just enough __*TEST CODE*__, including an error detail message (in "Assert" section), to observe a runtime __*ASSERTION FAILING*__ as expected against the application's incorrect return value.
6. Write just enough __*APPLICATION CODE*__, to observe the runtime __*ASSERTION PASSING*__, by correcting the return value; first iteration being hard-coded.
7. Refactor to remove (hard-coded) duplication.
8. Commit the small & focused change into the upstream code repository:
    ```
    git checkout master
    git merge --squash new-branch-name
    git commit -m "Commit message ..."
    git branch -D new-branch-name
    ```

---

* When on the fence over whether or not to put some code into its own method: do it, especially if it has any (branch) logic in it.  And TDD it into existence!
* When on the fence over whether or not to pre-process data, or process it at runtime, spike/tdd the common functionality before deciding.
* The `main` function is not TDDed; The application's `main` code is replaced by the unit tests' `main` code, and vice versa; The application's `main` code is tested at the user interface level (top) of the [test pyramid](https://en.wikipedia.org/wiki/Test_automation#Testing_at_different_levels).
