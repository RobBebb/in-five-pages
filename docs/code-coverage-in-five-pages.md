---
title: Code Coverage in Five Pages
author: Rob Bebbington
date: 12 July 2022
---

# Code Coverage in Five Pages

- [Code Coverage in Five Pages](#code-coverage-in-five-pages)
  - [Introduction](#introduction)
    - [What is Code Coverage?](#what-is-code-coverage)
  - [Installation](#installation)
  - [How To](#how-to)
    - [References](#references)

## Introduction

A concise document of setting up and checking code coverage in Flutter using VS Code.

### What is Code Coverage?

Code Coverage is checking to how much of the code is tested by the tests.

## Installation

Two VS Code extensions should be installed:

- Flutter Coverage
- Coverage Gutters

It is best to add `coverage/lcov.info` to the `.gitignore` file to prevent the code coverage data being version controlled.

## How To

To generate the code coverage data run `flutter test --coverage` in the terminal.

To view the output look under testing in the primary side bar. There will be a FLUTTER COVERAGE section at the bottom. This information is generated from the lib\coverage\lcov.data file which is generated when you run the above command.

To view the coverage of a specific file, open the file and click the Watch button at the bottom of the screen and the coverage for file will be shown in the gutter. Code covered (tested) is shown in green and code not covered (not tested) is shown in red.

### References
