---
title: FlutterFire in Five Pages
author: Rob Bebbington
date: 30 February 2021
---

# FlutterFire in Five Pages

- [Introduction](#introduction)
  - [What is FlutterFire?](#what-is-flutterfire)
- [Installation](#installation)
  - [Dependencies](#dependencies)
  - [Web Requirements](#web-requirements)
- [How To](#how-to)
  - [Initialise FlutterFire](#initialise-flutterfire)
  - [Firebase Auth Instance](#firebase-auth-instance)
  - [Cloud Firestore Instance](#cloud-firestore-instance)
- [References](#references)

## Introduction

A concise document of the main FlutterFire features and commands that I use.

### What is FlutterFire?

FlutterFire is a set of Flutter plugins which connect your Flutter application to Firebase.

## Installation

Before using Firebase a project need to be defined in Firebase. Use the [Firebase console](https://console.firebase.google.com/) to do this.

Then Firebase needs to be configured for whatever platform you will be working with:

- [Android](https://firebase.flutter.dev/docs/installation/android)
- [iOS](https://firebase.flutter.dev/docs/installation/ios)
- [MacOS](https://firebase.flutter.dev/docs/installation/macos)
- [Web](https://firebase.flutter.dev/docs/installation/web)

### Dependencies

For any Firebase service add the `firebase_core` plugin, which is responsible for connecting your application to Firebase, to your pubspec.yaml file.

For the Firebase authentication service add the `firebase_auth` plugin, which supplies backend services & easy-to-use SDKs to authenticate users, to your pubspec.yaml file.

For Cloud Firestore service add the `cloud_firestore` plugin to your pubspec.yaml file. Firestore is a flexible, scalable NoSQL cloud database to store and sync data. It keeps your data in sync across client apps through realtime listeners and offers offline support so you can build responsive apps that work regardless of network latency or Internet connectivity.

```yaml
dependencies:
  flutter:
    sdk: flutter
  firebase_core: "^1.7.0"
  firebase_auth: "^3.1.2"
  cloud_firestore: "^2.5.3"
  ```

and run `flutter pub get`.

### Web Requirements

To use any Firebase service on the web add `firebase-app` JavaScript SDK to the index.html file.

To use Firebase authentication on the web add `firebase-auth` JavaScript SDK to the index.html file.

To use Cloud Firestore on the web add `firebase-firestore` JavaScript SDK to the index.html file.

```html
<html>
  ...
  <body>
    <script src="https://www.gstatic.com/firebasejs/8.6.1/firebase-app.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.6.1/firebase-auth.js"></script>
    <script src="https://www.gstatic.com/firebasejs/8.6.1/firebase-firestore.js"></script>
  </body>
</html>
```

## How To

### Initialise FlutterFire

FlutterFire needs to be initialised before any firebase service can be used.

Import `package:firebase_core/firebase_core.dart` and call `initializeApp` method on the `Firebase` class:

```dart
await Firebase.initializeApp();
```

For further details about using a FutureBuilder or a stateful widget to await see [FlutterFire Overview](https://firebase.flutter.dev/docs/overview).

### Firebase Auth Instance

Import `package:firebase_auth/firebase_auth.dart` and call the `instance` getter on the `FirebaseAuth` class:

```dart
FirebaseAuth auth = FirebaseAuth.instance;
```

For further details see [Firebase Authentication Usage](https://firebase.flutter.dev/docs/auth/usage).

### Cloud Firestore Instance

Import `package:cloud_firestore/cloud_firestore.dart` and call the `instance` getter on the `FirebaseFirestore` class:

```dart
FirebaseFirestore firestore = FirebaseFirestore.instance;
```

For further details see [Cloud Firebase Usage](https://firebase.flutter.dev/docs/firestore/usage).

## References

- [FlutterFire home page](https://firebase.flutter.dev/)
