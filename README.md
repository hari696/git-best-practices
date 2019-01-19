Git Best Practices
============

A guide for developers on using version control system.

Standard Guidelines
---------------

* Use `_` or `-` as separations for repo and branch names.
* Always start your work at new branch.
* Choose rebase and merge respective to branches.
* Maintain separate branch for development, staging and production.
* Provide proper tags and release versions.

Work Practice
---------------

Create a local `feature` branch based off `master`.

    git checkout master
    git pull
    git checkout -b <branch-name>

Rebase frequently to incorporate upstream changes.

    git fetch origin
    git rebase origin/master

Resolve conflicts. When feature is complete and tests pass, stage the changes.

    git add --all

When you've staged the changes, commit them.

    git status
    git commit --verbose

Write a [good commit message]. Example format:

    Present-tense summary under 50 characters

    * More information about commit (under 72 characters).
    * More information about commit (under 72 characters).

    http://project.management-system.com/ticket/123

If you've created more than one commit,
[use `git rebase` interactively](https://help.github.com/articles/about-git-rebase/)
to squash them into cohesive commits with good messages:

    git rebase -i origin/master

Share your branch.

    git push origin <branch-name>

Submit a [GitHub pull request].

Ask for a code review in the project's chat room.

Repo Management
---------------

* Avoid including files in source control that are specific to your
  development machine or process.
* Delete local and remote feature branches after merging.
* Perform work in a feature branch.
* Rebase frequently to incorporate upstream changes.
* Use a [pull request] for code reviews.

[pull request]: https://help.github.com/articles/using-pull-requests/

Pull Request Mangement
---------------
* Each `pull request` should pass code review and unit test before merging to `master` branch.
* Make use of labels to define the type of PR (Feature, Bug, Enhancement and so on).
* Always get both code and feature reivew from previous developer of the file for new changes.
* Make sure to run unit test in master branch after merging feature branch.

Use Frequently
---------------

Try to use these commands frequently while developing.

    git fetch origin
    git checkout master
    git pull origin master
    git rebase -i master (In feature branch)

Git Cheat Sheet
---------------

Download [Git Cheat Code](https://www.atlassian.com/dam/jcr:8132028b-024f-4b6b-953e-e68fcce0c5fa/atlassian-git-cheatsheet.pdf) in pdf format and practice regularly.

Agile Development
---------------

Follow these techniques or best practices to maintain continues development and release

* Maintain one or more stable branch to release at any time instance.
* Run unit and feature driven test on each and every PR.
* Assign code reviewers for each module or set of developers.
* Block user's push to stable remote branch.
* Use automation jobs for continues testing and deployment process.

Other References
---------------

* [Tutorial](https://git-scm.com/docs)
* [Code Review](https://github.com/thoughtbot/guides/tree/master/code-review)
* [Style Guide](https://github.com/thoughtbot/guides/tree/master/style)
* [Programmers Guide](https://github.com/mtdvio/every-programmer-should-know)

[good commit message]: https://wiki.gnome.org/Git/CommitMessages
[GitHub pull request]: https://help.github.com/articles/using-pull-requests/
