# Git Hooks

`Git Hooks` are scripts that run before or after certain events in a Git repository.

![Image](img/git-hooks.png)

## Contents

* [Dependencies](#dependencies)
* [Why?](#why)
* [Commit-msg](#commit-msg)
* [Pre-commit](pre-commit)
* [Summary](summary)
  
## Dependencies

* [Python 3.*+](http://python.org/downloads)
* Linux (ex. Ubuntu)
* Git 2.3

## Why?

The goal is to use Git Hooks to improve software development. To do this, Git Hooks are used to automate the following tasks:

* **Linting:** Running a linter tool to verify compliance with style guidelines.
* **Formation:** Running a formater tool to verify compliance with style guidelines.
* **Automatic Testing:** Running unit tests to verify the functionality of the changes.

## Commit-msg

Follow and apply the commit-message rules and patterns :
<https://www.conventionalcommits.org/en/v1.0.0/>

* type: description (Max 50 char)
* type(scope): description (Max 50 char) — (scope) is optional

What are the Commit-message types?

* feat (new feature)
* fix (bug fix)
* refactor (refactoring production code)
* style (formatting, missing semi colons, etc; no code change)
* docs (changes to documentation)
* test (adding or refactoring tests; no production code change)
* chore (change buildtools, dependencies, delete files; no production code change)
* wip (work in progress commit to be squashed — do not push!)

### Commit-msg installation

* Download git-hook repo <https://github.com/avionic-design/git-hooks/>
* To install the hook, you can either create a symlink to it in . git/hooks , or you can simply copy and paste it into the .git/hooks directory whenever the hook is updated.
* Git hooks are triggered automatically

## Pre-commit

Pre-commit hooks are small scripts or commands that are executed before a version control system commits changes to a codebase. These hooks allow developers to enforce coding standards, run tests, or perform other checks on their code before it is committed. They help ensure that only high-quality and compliant code is added to the repository, reducing the chances of introducing bugs or issues.

### Pre-Commit installation

All the following tools (Framework, Python, Bash, and C) need to be installed.

#### Pre-commit Framework <https://pre-commit.com/>

Pre-commit is a framework for managing and automating pre-commit hooks. It provides a simple and configurable way to define and run custom checks on your codebase before each commit. Pre-commit integrates seamlessly into your development workflow and can be used with a wide range of programming languages and tools.

Installation:

```console
pip install pre-commit
```

#### Pre-commit for python

Style Guide:

* PEP 8 <https://peps.python.org/pep-0008/#documentation-strings>

Tools:

* Linter = ruff: An extremely fast Python linter, written in Rust <https://github.com/astral-sh/ruff#getting-started>
* Formatter = black <https://github.com/psf/black>

Installation:

```console
pip install ruff black
```

#### Pre-commit for bash

Style Guide:

* <https://google.github.io/styleguide/shellguide.html>

Tools:

* Linter = shellcheck <https://github.com/koalaman/shellcheck>
* Formatter = shfmt <https://github.com/patrickvane/shfmt>

Installation:

```console
sudo apt install -y shellcheck
sudo apt-get -y install shfmt
```

#### Pre-commit for C

Style Guide:

* Linux kernel coding style <https://www.kernel.org/doc/html/v4.10/process/coding-style.html>

Tools:

* Linter = cpplint <https://github.com/cpplint/cpplint>
* Formatter = clang-format

Installation:

```console
pip install cpplint
sudo apt install clang-format
```

### Configuration

* Download .pre-commit-config.yaml <https://github.com/avionic-design/git-hooks/tree/main/config>
* Place the .pre-commit-config.yaml file in the root directory of your Git project.
* 
```console
pre-commit install
```
## Summary

Using Git Hooks can improve software development in many ways. However, it is important to consider the drawbacks of Git Hooks and implement the hooks properly to avoid security risks.
