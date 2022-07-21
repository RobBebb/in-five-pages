---
title: Dart Command Line Apps in Five Pages
author: Rob Bebbington
date: 20 July 2022
---

# Dart Command Line Apps in Five Pages

- [Dart Command Line Apps in Five Pages](#dart-command-line-apps-in-five-pages)
  - [Introduction](#introduction)
  - [How To](#how-to)
    - [Add equality, hashCode, to String etc. to exisiting class](#add-equality-hashcode-to-string-etc-to-exisiting-class)
    - [References](#references)

## Introduction

A concise document of Dart Command Line Apps.

## How To

### Create an App

Go to the folder you would like to use for the app and run `dart create -t console xxxxx` where xxxxx is the app name.

This creates a folder xxxxx for the app with a main source file bin/xxxxx.dart that contains the top-level main() function, the entrypoint for the app.

An additional dart file, lib/xxxxx.dart contains the functionality of the app.

### Run the App

Change to the `xxxxx` folder and run the command `dart run`. This builds and runs the app.

### Compile for Production

In the `xxxxx` folder run the command `dart compile exe bin/xxxxx.dart`.

### Run the compiled app

Change to the `bin` folder and enter `xxxxx`.

## References

- [Get started](https://dart.dev/tutorials/server/get-started)
