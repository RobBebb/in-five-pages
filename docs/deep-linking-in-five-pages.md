---
title: Deep Linking in Five Pages
author: Rob Bebbington
date: 22 October 2021
---

# Deep Linking in Five Pages

- [Deep Linking in Five Pages](#deep-linking-in-five-pages)
  - [Introduction](#introduction)
    - [What is Deep Linking?](#what-is-deep-linking)
  - [Installation](#installation)
  - [How To](#how-to)
    - [Link to the home page](#link-to-the-home-page)
  - [References](#references)

## Introduction

A deep link is a URL that navigates to a specific destination in your mobile app. You can think of deep links like a URL address you enter into a web browser to go to a specific page of a website rather than the home page.

### What is Deep Linking?

A deep link is a URL that navigates to a specific destination in your mobile app. You can think of deep links like a URL address you enter into a web browser to go to a specific page of a website rather than the home page.

## Installation

To test deep links on Android the adb.exe is used. This is installed with Android Studio and is in `C:\Users\Rob\AppData\Local\Android\Sdk\platform-tools\`

## How To

### Link to the home page

Enter a command like `C:\Users\Rob\AppData\Local\Android\Sdk\platform-tools\adb shell am start -a android.intent.action.VIEW -c android.intent.category.BROWSABLE -d 'fooderlich://raywenderlich.com/home?tab=1'`

```cmd
C:\Users\Rob\AppData\Local\Android\Sdk\platform-tools\adb shell am start ^
-a android.intent.action.VIEW ^
-c android.intent.category.BROWSABLE ^
-d 'fooderlich://raywenderlich.com/home?tab=1'
```

```powershell
C:\Users\Rob\AppData\Local\Android\Sdk\platform-tools\adb shell am start `
-a android.intent.action.VIEW `
-c android.intent.category.BROWSABLE `
-d 'fooderlich://raywenderlich.com/home?tab=1'
```

```bash
~/AppData/Local/Android/sdk/platform-tools/adb shell am start -a android.intent.action.VIEW \
-c android.intent.category.BROWSABLE \
-d 'fooderlich://raywenderlich.com/home?tab=1'
```

## References

- [Xxxxxx home page](https://flutter.dev/)
