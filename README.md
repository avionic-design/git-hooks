# Git Hooks

Git Hooks are scripts that run automatically when certain events happen in a Git repository. You can use them to automate tasks like running linters, running unit tests, or triggering a code review process.

For more information about Git Hooks, see the Git Hooks: git-hooks.md documentation.

## Dependencies

* [Python 3.*+](http://python.org/downloads)
* Linux (ex. Ubuntu)
* Git 2.3

## Usage

### Installation & Configuration

* Download hook
* Make sure filename is **commit-msg**
* Make chosen file executable using **chmod 755 commit-msg**
* Put the file into every project you want to use githook for. Destination folder looks like: **your_project/.git/hooks**
* Alternatively, you can **specify general folder** for git to look for hooks instead of putting them into every project .git/hooks folder.
  * Use command below with path to your global hooks directory
    * ```git config --global core.hooksPath /usr/local/.../git/hooks```

### Executing

Git hooks are triggered automatically if they are located in .git directory in your repository or in global folder.
