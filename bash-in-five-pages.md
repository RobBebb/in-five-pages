---
title: Bash in Five Pages
author: Rob Bebbington
date: 24 February 2021
---

## Contents

## Introduction

A concise document of the main Bash features and commands that I use.

### What is Bash?

Bash is a command line interpreter for the GNU operating systen (Linux).

## Installation

I installed it as part of the [Git](https://git-scm.com) package from their website.

For further details about configurations for GIT see Git in Five Minutes.

## How To

Display the current working directory - `pwd`

List the details of a file - `cat <filename>`. `cat` can also be used to create files and concatenaye files together.

Rename a file - `mv <oldfilename> <newfilename>`

Delete a file - `del <filename>` or `rm <filename>`

Create a directory - `mkdir <directoryname>`

Remove an empty directory - `rmdir <directoryname>`

Remove a directory with contents - `rm -rf <directoryname>`. The `-r` recursively removes all files and subdirectories. The `-f` removes the files and subdirectories without prompting for confirmation. Be careful.

List files and directories, including hidden ones - `ls -la`. The `-l` gives a long listing which has extra information. The `-a` lists hidden files and directories.

Move a file - `mv <sourcefile> <destinationfile>`

### References

* [GNU Bash website](https://www.gnu.org/software/bash/)
* [The manual](https://www.gnu.org/software/bash/manual)
