# Android App for Flarum

> A way to build an Android app for your flarum site easily.

## About this project:
 This project is designed for the webmasters of Flarum websites. This project can help the Flarum website owners to build their web-based Android apps easily, and help the Flarum websites to keep the users. It mainly used the 'webview' tech in Java, with cache storage, log in protection, and other techs. Note: This is not a Flarum official project.

## What is Flarum?
**[Flarum](https://flarum.org/) is a delightfully simple discussion platform for your website.** It's fast and easy to use, with all the features you need to run a successful community. It is designed to be:

* **Fast and simple.** No clutter, no bloat, no complex dependencies. Flarum is built with PHP so it’s quick and easy to deploy. The interface is powered by Mithril, a performant JavaScript framework with a tiny footprint.

* **Beautiful and responsive.** This is forum software for humans. Flarum is carefully designed to be consistent and intuitive across platforms, out-of-the-box.

* **Powerful and extensible.** Customize, extend, and integrate Flarum to suit your community. Flarum’s architecture is amazingly flexible, with a powerful Extension API.

## How to build an app with this project?
> We have found two approaches for you to use this project, a command-line more approach, and a applications more approach.

We'll start with the **command-line approach**, to skip to the application approach, click here. The command line approach allows you to:
* **Add your website url**
* **Change the name of the app**
* **Make the app with any operating system gradle support**

This approach doesn't allow you to:

* **Use custom icon for the app**
* **Customize your app package name**
* **Add custom functions to your generated app**

Here is how the easier approach:
1. Make sure you have Gradle installed on your device, to check if you have installed, or not, run the following command through the command line:
    
    >  gradlew -v
   
   If there **are** info about gradle, congragulations, you can skip the installation of gradle, if there isn't, follow the following instruction:
   1. If you are a **Linux/GNU** user, the system might tell you if you want to install gradle, after you ran the previous command, if it didn't, follow this guide to install gradle in your device: https://gradle.org/install
   2. If you are a **Windows/Mac** user, you can follow the official guide to install: https://gradle.org/releases/ , or https://gradle.org/install
   
   ** Note: You need to add gradle as a path when installing it.**
   ** Note: You need to install [Java](https://java.com) before installation of gradle.**
   
2. After gradle is prepared, there is only a little things need to be done.
   1. Download the release of this project:
      
      ```git clone https://github.com/Aurorum-Studio/flarum-app.git```    ##using git
      
      or,
      
      Directly dowload the latest release from GitHub: https://github.com/Aurorum-Studio/flarum-app/releases/
      
   2. Now it's time to customize your app, 
    
      > First, go to (relative path) /app/src/main/res/values/strings.xml
      
      > You can open this file with almost any text editor, and change the "My Flarum" on the second line "<string name="app_name">My Flarum</string>", into the qpp name   you want.
      
      > **This step is very important**, go to (relative path) /app/src/main/java/com/hhilan/flarum/MainActivity.java
      > Change "https://www.hhilan.com" on line 23, to your own url (the link of your website homepage).
      
      **Warning: Do not change anything else in this file, unless you KNOW WHAT YOU'RE DOING.**
      
   3. If you're a Windows user, simply double-click the build.cmd file, and the building process would run automatically.
   
      If you're a Linux/GNU user, open the command line in the folder of this project, and run the following command:
      
      ```gradlew clean```
      ```gradlew build```
      
Then, the app will be generate automatically, after the command line is closed (on Windows), or start a new line (on Linux/GNU), your app is already generated.

You can find your app for debugging in (relative path) /app/build/outputs/apk/debug/app-debug.apk

You can find your app for release in (relative path) /app/build/outputs/apk/debug/app-release-unsigned.apk

**Note: It's recommanded to use debug app instead of the released one, because the released one is unsigned.**
