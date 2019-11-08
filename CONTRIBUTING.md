# Contributing

Looking to contribute something? **Here's how you can help.**

Please take a moment to review this document in order to make the contribution
process easy and effective for everyone involved.

Following these guidelines helps to communicate that you respect the time of
the developers managing and developing this open source project. In return,
they should reciprocate that respect in addressing your issue or assessing
patches and features.

## Code of Conduct

Help us keep this community open and inclusive. Please read and follow our
[Code of Conduct](https://github.com/xtreamwayz/.github/blob/master/CODE_OF_CONDUCT.md).

## Using the issue tracker

The issue tracker is the preferred channel for [bug reports](#bug-reports),
[features requests](#feature-requests) and [submitting pull requests](#pull-requests),
but please respect the following restrictions:

* Please **do not** derail or troll issues. Keep the discussion on topic and
  respect the opinions of others.

* Please **do not** post comments consisting solely of "+1" or ":thumbsup:".
  Use [GitHub's "reactions" feature](https://blog.github.com/2016-03-10-add-reactions-to-pull-requests-issues-and-comments/)
  instead. We reserve the right to delete comments which violate this rule.

## Bug reports

A bug is a _demonstrable problem_ that is caused by the code in the repository.
Good bug reports are extremely helpful, so thanks!

Guidelines for bug reports:

0. **Validate you code** to ensure your problem isn't caused by a simple error
   in your own code.

1. **Use the GitHub issue search** &mdash; check if the issue has already been
   reported.

2. **Check if the issue has been fixed** &mdash; try to reproduce it using the
   latest `master` or development branch in the repository.

3. **Isolate the problem** &mdash; ideally create a reduced test case to
   demonstrate the bug.

## Feature requests

Feature requests are welcome. But take a moment to find out whether your idea
fits with the scope and aims of the project. It's up to *you* to make a strong
case to convince the project's developers of the merits of this feature. Please
provide as much detail and context as possible. Our time is limited but we are
open for [pull requests](#pull-requests).

## Pull requests

Good pull requests—patches, improvements, new features—are a fantastic
help. They should remain focused in scope and avoid containing unrelated
commits.

**Please ask first** before embarking on any significant pull request (e.g.
implementing features, refactoring code), otherwise you risk spending a lot of
time working on something that the project's developers might not want to merge
into the project.

Please adhere to the [coding rules](#coding-rules) used throughout the
project (indentation, accurate comments, etc.) and any other requirements
(such as test coverage).

Adhering to the following process is the best way to get your work
included in the project:

1. [Fork](https://help.github.com/articles/fork-a-repo/) the project, clone your
   fork, and configure the remotes:

   ```bash
   # Clone your fork of the repo into the current directory
   git clone https://github.com/<your-username>/<project>.git
   # Navigate to the newly cloned directory
   cd <project>
   # Assign the original repo to a remote called "upstream"
   git remote add upstream https://github.com/xtreamwayz/<project>.git
   ```

2. If you cloned a while ago, get the latest changes from upstream:

   ```bash
   git checkout master
   git pull upstream master
   git rebase upstream/master
   # And optionally, to update your fork
   git push origin master:master
   ```

3. Create a new topic branch (off the main project development branch) to
   contain your feature, change, or fix:

   ```bash
   git checkout -b <topic-branch-name>
   ```

4. Commit your changes in logical chunks. Please adhere to the
   [conventional commits specification](#commit-message-format)
   or your code is unlikely be merged into the main project. Use Git's
   [interactive rebase](https://help.github.com/articles/about-git-rebase/)
   feature to tidy up your commits before making them public.

5. Locally merge (or rebase) the upstream branch into your topic branch:

   ```bash
   git pull [--rebase] upstream master
   ```

6. Push your topic branch up to your fork:

   ```bash
   git push origin <topic-branch-name>
   ```

7. [Open a Pull Request](https://help.github.com/articles/about-pull-requests/)
    with a clear title and description against the `master` branch.

**IMPORTANT**: By submitting a patch, you agree to allow the project owners to
license your work under the terms of the [MIT License](../LICENSE.md) (if it
includes code changes) and under the terms of the
[Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)
(if it includes documentation changes).

## Coding Rules

To ensure consistency throughout the source code, keep these rules in mind as you are working:

- All features or bug fixes must be tested by one or more unit-tests.
- We follow the [Zend Coding Standard](https://github.com/zendframework/zend-coding-standard) for PHP,
  the [airbnb base standard](https://github.com/airbnb/javascript) for JavaScript
  and the [Code Guide](https://codeguide.co/) for [HTML](https://codeguide.co/#html)
  and [CSS](https://codeguide.co/#css).

## Commit Message Format

Each commit message consists of a **header**, a **body** and a **footer**.
The header has a special format that includes a **type**, a **scope** and
a **subject**:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

The **header** is mandatory and the **scope** of the header is optional.

The footer should contain a [closing reference to an issue](https://help.github.com/articles/closing-issues-via-commit-messages/) if any.

Samples: (even more [samples](https://github.com/conventional-commits/conventionalcommits.org/commits/master))

```
docs(changelog): update changelog to 1.0.0-alpha.1
```
```
fix: need to depend on latest rxjs and zone.js

The version in our package.json gets copied to the one we publish, and users
need the latest of these.

closes #1
```

### Revert

If the commit reverts a previous commit, it should begin with `revert: `,
followed by the header of the reverted commit. In the body it should say:
`This reverts commit <hash>.`, where the hash is the SHA of the commit
being reverted.

### Type

Must be one of the following:

* **build**: Changes that affect the build system or external dependencies (example scopes: composer, npm)
* **ci**: Changes to our CI configuration files and scripts (example scopes: GitHub Actions, Circle, Travis)
* **docs**: Documentation only changes
* **feat**: A new feature
* **fix**: A bug fix
* **perf**: A code change that improves performance
* **refactor**: A code change that neither fixes a bug nor adds a feature
* **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)
* **test**: Adding missing tests or correcting existing tests
