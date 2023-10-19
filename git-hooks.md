# Git Hooks

## Goal

The goal of this concept is to use Git Hooks to improve software development. To do this, Git Hooks are used to automate the following tasks:

- **Linting:** Running a linter tool to verify compliance with style guidelines.
- **Automatic Testing:** Running unit tests to verify the functionality of the changes.
- **Code Review:** Triggering a code review process to verify the quality of the changes.
- **Deployment:** Deploying the changes to a production server.

## Benefits

Using Git Hooks can improve software development in the following ways:

- **Automation:** Git Hooks can automate repetitive tasks, such as running linter tools or running unit tests.
- **Quality:** Git Hooks can help improve the quality of software by checking for compliance with style guides, functionality of changes, and quality of code.
- **Efficiency:** Git Hooks can improve the efficiency of software development by saving developers time and effort.

## Downsides

Using Git Hooks can also have the following disadvantages:

- **Complexity:** Git Hooks can be complex if they are intended to automate large tasks.

- **Security:** Git Hooks can pose security risks if not implemented properly.

## Implementation steps

Step 1:

- Implementation of simple hooks:
  - commit-msg:
    - check syntax
  - Pre-commit hook:
    - run a linter tool
    - run unit tests

- Standardization

  Define a standardization for the use of Git Hooks in the project:

  - The names of the Git Hooks
  - The configuration files of the Git Hooks
  - The way the git hooks are used

- Tests of the Git Hooks!

## commit-msg

Follow and apply the commit-message rules and patterns :
<https://www.conventionalcommits.org/en/v1.0.0/>

- type: description (Max 50 char)
- type(scope): description (Max 50 char) — (scope) is optional

What are the Commit-message types?

- feat (new feature)
- fix (bug fix)
- refactor (refactoring production code)
- style (formatting, missing semi colons, etc; no code change)
- docs (changes to documentation)
- test (adding or refactoring tests; no production code change)
- chore (updating grunt tasks etc; no production code change)
- wip (work in progress commit to be squashed — do not push!)

## pre-commit

Git hook scripts are useful for identifying simple issues before submission to code review. We run our hooks on every commit to automatically point out issues in code. By pointing these issues out before code review, this allows a code reviewer to focus on the architecture of a change while not wasting time with trivial style nitpicks.

  <https://pre-commit.com/>

  A framework for managing and maintaining multi-language pre-commit hooks.

  <https://interrupt.memfault.com/blog/pre-commit>

### python

Tool = ruff <https://github.com/astral-sh/ruff#getting-started>

An extremely fast Python linter and formatter, written in Rust.

To comply with the regulations of the PEP 8 – Style Guide for Python Code
<https://peps.python.org/pep-0008/#documentation-strings>

## Summary

Using Git Hooks can improve software development in many ways. However, it is important to consider the drawbacks of Git Hooks and implement the hooks properly to avoid security risks.
