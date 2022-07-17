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
  - [Flutter Packages](#flutter-packages)
    - [Development Packages](#development-packages)
    - [Possible Future Packages](#possible-future-packages)

## Introduction

A concise document of the technologies I am currently using or might use.

## Products

- Project planning
  - [Github Projects](https://github.com)
- Document workspace
  - [Dropbox](https://www.dropbox.com)
- Drawings
  - [draw.io](https://draw.io)
  - Diagrams saved to dropbox
- Architectural diagrams
  - The C4 model for visualising software architecture
  - [C4 model](https://c4model.com)
- UI Design
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
- Database - remote
  - [Firebase Cloud Firestore](https://firebase.google.com/products/firestore) or [MariaDB](https://mariadb.org)
- Remote services
  - [Firebase](https://firebase.google.com)
- Authentication
  - [Firebase Authentication](https://firebase.google.com/products/auth)

## VS Code Extensions

- Better Comments (! alert, ? query, \* highlight, TODO: todos)
- Coverage Gutters
- [Dart](dart-extension-in-five-pages.md)
- Dart Data Class Generator
- Dracula Official
- Error Lens
- Flutter
  - In the settings, enable the Dart:Preview Flutter Ui Guides option. That will make it really easy to spot the parent-child relationships in your code
- Flutter Coverage
- Flutter Intl
- Flutter Riverpod Snippets
- Git Graph
- Git History
- GitHub Pull Requests and Issues
- GitLens - Git supercharged
- Hex Editor
- Image preview
- indent-rainbow
- jshint
- LCOV.info language support
- Markdown All in One
- Markdown yaml Preamble
- Markdownlint
- Markdown yaml Preamble
- Material Icon Theme
- Prettify JSON
- Todo Tree
- vscode-pandoc
- vscode-pdf
- YAML

### VS Code Settings

- debug.toolBarLocation - set to docked so it doesn't float in the way of file name

## Flutter Packages

- [hive](https://pub.dev/packages/hive) - Lightweight and blazing fast key-value database written in pure Dart. Strongly encrypted using AES-256.
- [hive_flutter](https://pub.dev/packages/hive_flutter) - Flutter extension for Hive to make it easier to use hive in Flutter apps.
- [semblast](https://pub.dev/packages/sembast) - NoSQL persistent store database solution for single process io applications.
- [provider](https://pub.dev/packages/provider) - A wrapper around InheritedWidget to make them easier to use and more reusable.
- [riverpod](https://pub.dev/packages/riverpod) - A simple way to access state from anywhere in your application while robust and testable.
- [intl](https://pub.dev/packages/intl) - Contains code to deal with internationalized/localized messages, date and number formatting and parsing, bi-directional text, and other internationalization issues.
- [intl_utils](https://pub.dev/packages/intl_utils) - intl_utils is a dart library that generates Dart localization code from ARB file. Generated code relies on Intl library.
- [uuid](https://pub.dev/packages/uuid) - RFC4122 (v1, v4, v5) UUID Generator and Parser for all Dart platforms (Web, VM, Flutter)
- flutter_localizations
- [fl_chart](https://pub.dev/packages/fl_chart) - A powerful Flutter chart library, currently supporting Line Chart, Bar Chart and Pie Chart.
- [email_validator](https://pub.dev/packages/email_validator) - A simple (but correct) dart class for validating email addresses

### Development Packages

- [hive_generator](https://pub.dev/packages/hive_generator) - Extension for Hive. Automatically generates TypeAdapters to store any class.
- [test](https://pub.dev/packages/test) - A full featured library for writing and running Dart tests across platforms.
- [build_runner](https://pub.dev/packages/build_runner) - A build system for Dart code generation and modular compilation.
- [flutter_driver](https://api.flutter.dev/flutter/flutter_driver/flutter_driver-library.html) - Provides API to test Flutter applications that run on real devices and emulators.

### Possible Future Packages

- [pdf](https://pub.dev/packages/pdf) - A pdf producer for Dart. It can create pdf files for both web or flutter.
- [printing](https://pub.dev/packages/printing) - Plugin that allows Flutter apps to generate and print documents to compatible printers on Android, iOS, macOS, Windows, and Linux, as well as web print.
- [path_provider](https://pub.dev/packages/path_provider) - Flutter plugin for getting commonly used locations on host platform file systems, such as the temp and app data directories.
- [flutter_email_sender](https://pub.dev/packages/flutter_email_sender) - Allows send emails from flutter using native platform functionality.
- [excel](https://pub.dev/packages/excel) - A flutter and dart library for reading, creating, editing and updating excel sheets with compatible both on client and server side
- [table_calendar](https://pub.dev/packages/table_calendar) - Highly customizable, feature-packed calendar widget for Flutter.
- [url_launcher](https://pub.dev/packages/url_launcher) - Flutter plugin for launching a URL. Supports web, phone, SMS, and email schemes.
- [introduction_screen](https://pub.dev/packages/introduction_screen) - Introduction/Onboarding package for flutter app with some customizations possibilities
