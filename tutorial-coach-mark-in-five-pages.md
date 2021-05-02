---
title:Tutorial Coach Mark in Five Pages
author: Rob Bebbington
date: 2 May 2021
---

## Contents

## Introduction

A concise document on using Tutorial Coach Mark in a Flutter application.

### What is Tutorial Coach Mark?

Tutorial Coach Mark is a Flutter package that helps present your application and its features in a beautiful, simple and customisable way. It allows you to easily create a tutorial.

By specifying a `GlobalKey` on a widget Tutorial Coach Mark can display tutorial information for that widget. Tutorial Coach Mark takes the user from one widget to the next that have been defined as a target for the tutorial.

## Installation

Refer to the [pub.dev installing page for TutorialCoachMark](https://pub.dev/packages/tutorial_coach_mark/install).

## How To

### Add Tutorial for a page

A page is basically any `build` that returns a `Scaffold` widget. If you call other classes that return widgets within the `Scaffold` widget, they are part of the same page. If you want a widget in a called class to be a target you will need to pass the `GlobalKey` to the called class and add as a key for the widget.

1. Add an `import` to the dart file for the page

   ```Dart
   import 'package:tutorial_coach_mark/tutorial_coach_mark.dart';
   ```

2. Add a `GlobalKey` for each target widget for which inormation will be added

   ```Flutter
   final drawerKey = GlobalKey();
   ```

3. Add a `TutorialCoachMark` variable to the `State` class of the page

   ```Flutter
   TutorialCoachMark tutorialCoachMark;
   ```

4. Add a `List` of type `TargetFocus` to contain the targets for thew tutorial. A target is a widget for which tutorial information will be displayed.

   ```Flutter
   List<TargetFocus> targets = [];
   ```

5. Add the GlobalKeys to the key of the widgets

   ```Flutter
   leading: IconButton(
     icon: Icon(
       Icons.menu,
       key: drawerKey,
     ),
     onPressed: () {
       _scaffoldKey.currentState.openDrawer();
     },
   ),
   ```

6. Add a function to initialise the tutorial information for each target

   ```Flutter
   void initTargets() {
     targets = [];
     print('Add target 1');
     targets.add(
       TargetFocus(
         identify: 'Target 1',
         keyTarget: drawerKey,
         color: Theme.of(context).dialogBackgroundColor,
         contents: [
           TargetContent(
             align: ContentAlign.bottom,
             child: Container(
               child: Column(
                 mainAxisSize: MainAxisSize.min,
                 crossAxisAlignment: CrossAxisAlignment.start,
                 children: <Widget>[
                   Text(
                     'Tap this icon to bring up the menu.',
                     style: kCoachHeaderTextStyle,
                   ),
                   Padding(
                     padding: const EdgeInsets.only(top: 10.0),
                     child: Text(
                       'Use the menu to select options to add vessels, add jobs,create PDFs.',
                       style: kCoachBodyTextStyle,
                     ),
                   ),
                   SizedBox(height: 20.0),
                   Padding(
                     padding: const EdgeInsets.only(top: 10.0),
                     child: Text(
                       'Tap highlighted area to proceed, tap SKIP to close help.',
                       style: kCoachFooterTextStyle,
                     ),
                   )
                 ],
               ),
             ),
           )
         ],
         shape: ShapeLightFocus.RRect,
         radius: 5,
       ),
     );
   }
   ```

7. Add a call to the `initTargets` function. Maybe in the `didChangeDependencies` method.

   ```Flutter
   initTargets();
   ```

8. Add a function to show the tutorial.

   ```Flutter
   void showTutorial() {
     tutorialCoachMark = TutorialCoachMark(
       context,
       targets: targets,
       colorShadow: Colors.red,
       textSkip: "SKIP",
       textStyleSkip: kCoachSkipTextStyle,
       paddingFocus: 10,
       opacityShadow: 0.8,
       onFinish: () {
         print("finish");
       },
       onClickTarget: (target) {
         print('onClickTarget: $target');
       },
       onSkip: () {
         print("skip");
       },
       onClickOverlay: (target) {
         print('onClickOverlay: $target');
       },
     )..show();
   }
   ```

9. Add a way to show the tutorial - maybe a button in actions of the appbar

   ```Flutter
   IconButton(
     icon: Image.asset('assets/images/help-48.png'),
     onPressed: () {
       showTutorial();
     },
   ),
   ```

### Where the tutorial is displayed

The tutorial information is displayed in relation to the widget that has the global key for each target. The `align` property is used and can be set to `bottom`, `custom`, `left`, `right` or `top` using `ContentAlign` enum.

* `bottom` displays the tutorial below the widget
* `left` displays the tutorial to the left of the widget
* `right` displays the tutorial to the right of the widget
* `top` displays the tutorial above the widget
* `custom` allows you to specify exactly where to display it

For `custom` you also need to specify the `customPosition` property using `CustomTargetContentPosition` class. To display the tutorial information 10 pixels down from the top use:

   ```Flutter
   align: ContentAlign.custom,
   customPosition: CustomTargetContentPosition(top: 10.00),
   ```

## References

* [TutorialCoachMark readme](https://pub.dev/packages/tutorial_coach_mark)
