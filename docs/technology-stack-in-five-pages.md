---
title: Technology Stack in Five Pages
author: Rob Bebbington
date: 24 February 2021
---

# Technology Stack in Five Pages

- [Technology Stack in Five Pages](#technology-stack-in-five-pages)
  - [Introduction](#introduction)
  - [Products](#products)
  - [VS Code Extensions](#vs-code-extensions)
    - [VS Code Settings](#vs-code-settings)
    - [Packages](#packages)
    - [Development Packages](#development-packages)
    - [Possible Future Packages](#possible-future-packages)

## Introduction

A concise document of the technologies I am currently using or might use.

## Products

- Project planning
  - [Zenkit](https://zenkit.com)
- Document workspace
  - [Dropbox](https://www.dropbox.com)
- Drawings
  - [draw.io](https://draw.io)
  - Diagrams saved to dropbox
- Architectural diagrams (if I need them)
  - The C4 model for visualising software architecture
  - [C4 model](https://c4model.com)
- UI Design
  - [Adobe XD](https://www.adobe.com/au/products/xd.html)
  - [Lunacy](https://icons8.com/lunacy)
- Version control
  - [Git](https://git-scm.com/)
  - [GitHub](https://github.com)
- Continuous integration
  - [codemagic](https://codemagic.io)
- Integrated Development Environment (IDE)
  - [Visual Studio Code](https://code.visualstudio.com)
- Language
  - [Dart](https://dart.dev)
- UI toolkit
  - [Flutter](https://flutter.dev)
- Database - local
  - [Hive](https://docs.hivedb.dev)
- Remote services
  - [Firebase](https://firebase.google.com)
- Database - remote
  - [Firebase Cloud Firestore](https://firebase.google.com/products/firestore) or [MariaDB](https://mariadb.org)
- Authentication
  - [Firebase Authentication](https://firebase.google.com/products/auth)

## VS Code Extensions

- Better Comments (! alert, ? query, \* highlight, TODO: todos)
- Bracket Pair Colorizer 2
- [Dart](dart-extension-in-five-pages.md)
- Dracula Official
- Error Lens
- Flutter
  - In the settings, enable the Dart:Preview Flutter Ui Guides option. That will make it really easy to spot the parent-child relationships in your code
- Flutter Intl
- GitHub Pull Requests and Issues
- GitLens - Git supercharged
- Image preview
- indent-rainbow
- Markdown All in One
- Markdownlint
- Markdown yaml Preamble
- Material Icon Theme
- Pubspec Assist
- Todo Tree
- vscode-pandoc
- vscode-pdf
- YAML

### VS Code Settings

- debug.toolBarLocation - set to docked so it doesn't float in the way of file name

### Packages

- hive - key-value database for user data
- hive_flutter - Flutter extension for Hive to make it easier to use
- provider - Used to create a business class to control interactions between the UI and the database
- intl - Deal with internationalised / localised date formatting
- uuid - UUID Generator for database keys
- flutter_localizations
- fl_chart - charting package
- intl_utils - generates intl code
- email_validator - validate email addresses

### Development Packages

- hive_generator - extension for Hive to generate TypeAdapters to store any class
- test - Write and run dart unit tests
- build_runner - Used to run hive generator
- flutter_driver - Used to run function tests

### Possible Future Packages

- pdf - to create a report
- printing - to print the pdf
- path_provider - to save the pdf
- flutter_email_sender - to email the pdf
- excel - to bulk load and to backup/export restore/import
- table_calendar - show calendar of events
- url_launcher - link to icons8
- introduction_screen - splash screen
