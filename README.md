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
- ~~Pull requests~~ Surprise! We're gonna learn pull requests today.
- Merge conflicts
- `.gitignore`
- ~~Forking~~ Surprise! We're gonna learn how to fork today.
- GitHub Issues & Projects

## Terms

**branch** - A branch is a line of development. We create our own branches from certain points in the code's "history" to work off of. In most cases they will be brought back into the `master` or`main` branch, but some groups use a `develop` branch to work off of and only merge into `main` when they do a release.

**clone** - A duplicate copy of the current version of the code that you copy to your local computer to edit. This comes with "copies" of all of the existing branches, too.

**commit** - A single point in history. Can be looked at like a save point. Commits allow you to observe changes to the code over time, and have messages associated with them that list the changes that were made (called "commit messages").

**git** - A source control system for groups of programmers to collaborate on code, and for individuals to create non-destructive, tracked changes to code over time. There are lots of source control systems, but Git is one of the most popular.

**github** - Not to be confused with Git. While Git is a version control system, GitHub is one of many places where you can host repositories on the internet, and it is one of the most well-known. You do not have to use GitHub to use Git. Check out [these alternatives](https://opensource.com/article/18/8/github-alternatives). You can also store repositories just on your own computer or on your local network.

**merge** - To combine code changes from one branch into another. Typically you merge a branch with new features or changes back into the branch of origin. In our example, we merge branches created by our participants into the `main` branch of the workshop repository.

**pull** - To bring "upstream" or "origin" changes down into your local branch. In this example, we pull from this GitHub workshop repository to our local machines.

**push** - To send changes in your local branch "upstream" to the "origin." In this example, we push from our local machines to this GitHub workshop repository.

**repository** - You can think of this at a high-level as a whole coding project, or a collection of code. Often called a "repo." Each school assignment could be a repository. A huge web application could be a repository. A bunch of small applications that work together in one big system might each be their own repository.

**source control/version control** - Systems that allow for changes in code to be tracked, authored, saved, restored, and combined. 

## Tutorial

This will serve as a reference for you while we complete the workshop. If you wish to use a command prompt or terminal window for your all your Git commands, they are outlined as we go along.

1. Ensure you've completed all the prerequisites above (installing Git, setting up a GitHub account, etc.)
2. Fork the repository onto your own account.
3. Open up your GitHub Desktop application or your terminal window.
5. Clone the repository into an empty folder on your computer (replace `the-new-developers` here with your username, e.g. `jmia` or `rodneybarnes`).
   - `git clone https://github.com/<the-new-developers>/jens-cool-guy-git-workshop.git`
6. Open the folder in the code editor of your choice. You are examining your very own `main` branch. Also take this opportunity to open `index.html` in your browser. This is what we will be adding to.
7. If we were working with a local branch, we could create a new branch and switch to it like this:
   - `git branch jens-new-cool-guy-branch`
   - `git checkout jens-new-cool-guy-branch`
   - Feel free to call your branch whatever you like, `jens-new-cool-guy-branch` is just a suggestion
**Instead, we're going to edit right in our own personal `main` branch.**
9. Create a new HTML file in the `pages/` folder of the repository, give it a unique name, and make whatever changes you like.
10. Add the files to your upcoming commit (this is called 'staging').
   - `git add -A`
11. Add a message to your commit.
   - `git commit -m "Do a groovy thing"`
12. Push your shiny new branch to the repository.
    - `git push -u origin <jens-new-cool-guy-branch>`
    - The `-u` in this command stands for "upstream," which establishes the initial connection between your local copy and GitHub.
13. Return to GitHub and your forked repository.
14. Click the "Pull Request" button.
15. Add any additional information and press "Create Pull Request."
16. Wait for the codemeisters to merge your changes. While you wait, why not check out [all the open source projects](https://github.com/explore) you'll be able to contribute to with your new skills?
17. When the changes are merged, issues are resolved, and commits are finished, watch as we switch back to the main branch.
    - `git checkout main`
19. We'll pull the changes that exist on GitHub into our local copy of the workshop repository.
    - `git pull`
20. Open our code editor to look at the new changes.

## References

- [Git Guides](https://github.com/git-guides/) - A great reference for major Git concepts and how to use them with GitHub and GitHub Desktop.

- [Git Terminology](https://git-scm.com/docs/gitglossary) - The official glossary for Git commands.
