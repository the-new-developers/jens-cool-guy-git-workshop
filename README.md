# The New Developers S04E02: Git and GitHub

by [@jmia](https://github.com/jmia) for [The New Developers](https://thenewdevelopers.com)

This tutorial is meant for beginners to Git and GitHub. Together we'll talk about some terminology and get our hands dirty with the basic concepts of source control.

## Overview

### Before We Start

This tutorial assumes you have... 

- A novice amount of experience with HTML & CSS
- A [GitHub account](https://github.com/join)
- Git [installed on your computer](https://github.com/git-guides/install-git)
  - Optionally, a GUI version of Git like [GitHub Desktop](https://github.com/git-guides/install-git#install-git-using-github-desktop) installed on your computer
- A code editor like [VS Code](https://code.visualstudio.com/) or [Notepad++](https://notepad-plus-plus.org/downloads/)

### What You'll Learn

By the end of this workshop, you should be able to...

- Clone a repository
- Create a branch
- Make a commit on a local branch
- Push a commit to a remote branch
- Fetch and pull from a remote branch
- Define all the terms used above

### After We're Done

Some next steps that aren't covered in this tutorial:

- Creating your own repository
- Pull requests
- Merge conflicts
- `.gitignore`
- Forking
- GitHub Issues & Projects

## Terms

**branch** - A branch is a line of development. We create our own branches from certain points in the code's "history" to work off of, with the assumption that eventually they will be brought back into the `master` or`main` branch.

**clone** - A duplicate copy of the current version of the code that you copy to your local computer to edit. Typically you make a branch after you clone.

**commit** - A single point in history. Can be looked at like a save point. Commits allow you to observe changes to the code over time, and have messages associated with them that list the changes that were made.

**git** - A source control system for groups of programmers to collaborate on code, and for individuals to create non-destructive, tracked changes to code over time.

**merge** - To combine code changes from one branch into another. Typically you merge a branch with new features or changes into the major branch that is the "source of truth."

**pull** - To bring "upstream" or "origin" changes down into your local branch.

**push** - To send changes in your local branch "upstream" to the "origin."

**repository** - This is normally defined as "a collection of references," but you can think of this simplistically as a whole code project, or a collection of code.

**source control** - Systems that allow for changes in code to be tracked, authored, saved, restored, and combined.

## Tutorial

This will serve as a reference for you while we complete the workshop. If you wish to use a command prompt or terminal window for your all your Git commands, they are outlined as we go along.

1. Ensure you've completed all the prerequisites above (installing Git, setting up a GitHub account, etc.)
2. Open up your GitHub Desktop application or your terminal window.
3. **Clone** the repository into an empty folder on your computer.
   - `git clone https://github.com/the-new-developers/jens-cool-guy-git-workshop.git`
4. Open the folder in the code editor of your choice. You are examining the `main` branch.
5. Before making any changes, create a new branch.
   - `git branch jens-new-cool-guy-branch`
6. Switch to the branch you just created.
   - `git checkout jens-new-cool-guy-branch`
7. Create a new HTML file in the `pages/` folder of the repository, give it a unique name, and make whatever changes you like.
8. Add the files to your upcoming commit (called 'staging').
   - `git add -A`
9. Add a message to your commit.
   - `git commit -m "Do a groovy thing"`
10. Push your shiny new branch to the repository.
    - `git push -u origin jens-new-cool-guy-branch`
    - The `-u` in this command stands for "upstream," which establishes the initial connection between your local copy and GitHub.
11. Wait for the showrunner (that's me) to merge your changes. While you wait, why not check out [all the open source projects](https://github.com/explore) you'll be able to contribute to with your new skills?
12. When the changes are merged, issues are resolved, and commits are finished, switch back to the main branch.
    - `git checkout main`
13. Preview all the new changes that were done to the code and its branches since you last checked out the code.
    - `git fetch`
14. Pull the changes that exist on GitHub into your local copy of the repository.
    - `git pull`
15. Open your code editor to look at the new changes.

## References

- [Git Guides](https://github.com/git-guides/) - A great reference for major Git concepts and how to use them with GitHub and GitHub Desktop.

- [Git Terminology](https://git-scm.com/docs/gitglossary) - The official glossary for Git commands.