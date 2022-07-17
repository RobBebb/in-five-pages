---
title: Git in Five Pages
author: Rob Bebbington
date: 24 February 2021
---

# Git in Five Pages

- [Introduction](#introduction)
  - [What is Git?](#what-is-git)
  - [What is GitHub?](#what-is-github)
- [Installation](#installation)
- [Commands](#commands)
  - [Help](#help)
- [How To](#how-to)
  - [Create Repository](#create-repository)
  - [Branch and Merge](#branch-and-merge)
  - [Stage and Commit](#stage-and-commit)
  - [Push and Pull](#push-and-pull)
  - [Stashes](#stashes)
  - [Tags](#tags)
  - [I Made a Mistake](#i-made-a-mistake)

## Introduction

A concise document of the main Git features and commands that I use.

### What is Git?

As per the [Git website](https://git-scm.com) "Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency."

The [Git website](https://git-scm.com) has the Pro Git book by Scott Chacon and Ben Straub available to [read online for free](https://git-scm.com/book/en/v2).

### What is GitHub?

As per [Wikipedia](https://en.wikipedia.org/wiki/GitHub) "GitHub, Inc. is a subsidiary of Microsoft which provides hosting for software development and version control using Git. It offers the distributed version control and source code management (SCM) functionality of Git, plus its own features. It provides access control and several collaboration features such as bug tracking, feature requests, task management, continuous integration and wikis for every project."

## Installation

Install from the [Git](https://git-scm.com) website.

Once installed you need to configure your identity(name and email) and editor(Visual Studio Code in my case). This should only need to be done once. Using Git Bash, enter:

```bash
git config --global user.name "Joe Soap"
git config --global user.email joesoap@example.com
git config --global core.editor "code --wait"
```

If the core.editor doesn't work as above, it use to be:
> core.editor="C:\Users\Rob\AppData\Local\Programs\Microsoft VS Code\Code.exe" --wait

To check your configuration enter:

```bash
git config --list --show-origin
```

The --show-origin option will display where the configuration setting was found.

## Commands

### Help

To get help use `git help <verb>` or to get help on the options for a specific command use `git config -h`. For example enter:

```bash
git help config
```

## How To

Create a new repository in an existing directory - `git init`
Clone a repository - `git clone <repositoryname>`
Find the status of a repository - `git status`
Add a new or modified file to be committed - `git add <filename>`
Add all
Update a remote repository - `git push`

### Create Repository

### Branch and Merge

1. Open Git Bash.
1. Change the current working directory to your local project.
1. Create a new branch "testing": `git branch testing`
1. Switch to the new branch: `git checkout testing`
1. The above two steps can be combined: `git checkout -b testing`
1. To merge testing back into master switch to master: `git checkout master` and merge: `git merge testing`
1. To look at the branch pointers: `git log --online --decorate`
1. Or to get more detail: `git log --online --decorate  --graph --all`
1. If there is a problem with the merge, to get more information: `git status`
1. To get a list of current branches use: `git branch`
1. If you need information about the last commit on each branch use the -v parameter: `git branch -v`

### Stage and Commit

### Push and Pull

### Stashes

### Tags

### I Made a Mistake
