<p align="center">
<a href="https://dev.aurorum.co"><img src="https://www.hhilan.com/assets/files/2023-02-18/1676725708-939590-20230218210810.png"></a>
</p>

# Android App for Flarum

> A way to build an Android app for your flarum site easily.

## About this project:
 This project is designed for the webmasters of Flarum websites. This project can help the Flarum website owners to build their web-based Android apps easily, and help the Flarum websites to keep the users. It mainly used the 'webview' tech in Java, with cache storage, log in protection, and other techs. Note: This is not a Flarum official project.

## What is Flarum?
**[Flarum](https://flarum.org/) is a delightfully simple discussion platform for your website.** It's fast and easy to use, with all the features you need to run a successful community. It is designed to be:

* **Fast and simple.** No clutter, no bloat, no complex dependencies. Flarum is built with PHP so it’s quick and easy to deploy. The interface is powered by Mithril, a performant JavaScript framework with a tiny footprint.

* **Beautiful and responsive.** This is forum software for humans. Flarum is carefully designed to be consistent and intuitive across platforms, out-of-the-box.

* **Powerful and extensible.** Customize, extend, and integrate Flarum to suit your community. Flarum’s architecture is amazingly flexible, with a powerful Extension API.

## Why this project is build?
> Currently, we have not found great Android app solution for Flarum, the only one we found is fluam/fluam_app, but it tends to be an app for a lot of websites, instead of one. Also, it's not avaliable for users to login, nor make any actions through that project. Thus, we build this simple project to help the Flarum webmasters to build apps for their own websites.

## How to build an app with this project?
> We have found two approaches for you to use this project, a command-line more approach, and a applications more approach.

### We'll start with the **command-line approach**, to skip to the application approach, click here. The command line approach allows you to:
* **Add your website url**
* **Change the name of the app**
* **Make the app with any operating system gradle support**

This approach doesn't allow you to:

* **Use custom icon for the app**
* **Customize your app package name**
* **Add custom functions to your generated app**

Here is instruction of the command-line approach:
1. Make sure you have Gradle installed on your device, to check if you have installed, or not, run the following command through the command line:
    
    >  gradlew -v
   
   If there **are** info about gradle, congragulations, you can skip the installation of gradle, if there isn't, follow the following instruction:
   1. If you are a **Linux/GNU** user, the system might tell you if you want to install gradle, after you ran the previous command, if it didn't, follow this guide to install gradle in your device: https://gradle.org/install
   2. If you are a **Windows/Mac** user, you can follow the official guide to install: https://gradle.org/releases/ , or https://gradle.org/install
   
   **Note: You need to add gradle as a path when installing it.**
   **Note: You need to install [Java](https://java.com) before installation of gradle.**
   
2. After gradle is prepared, there is only a little things need to be done.
   1. Download the release of this project:
      
      ```git clone https://github.com/Aurorum-Studio/flarum-app.git```    ##using git
      
      or,
      
      Directly dowload the latest release from GitHub: https://github.com/Aurorum-Studio/flarum-app/releases/
      
   2. Now it's time to customize your app, 
    
      > First, go to (relative path) /app/src/main/res/values/strings.xml
      
      > You can open this file with almost any text editor, and change the "My Flarum" on the second line "<string name="app_name">My Flarum</string>", into the app name   you want.
      
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

-----

### Now let's go to  start with the **application approach**. The application approach allows you to:
* **Add your website url**
* **Change the name of the app**
* **Use custom icon for the app**
* **Customize your app package name**
* **Add custom functions to your generated app**

This approach doesn't allow you to:

* **Make the app with any operating system gradle support.**
* **Generate your application with only a little disk storage cost.**

Here is the **application approach** instruction:
1. Download and install Android Studio, the official release and install instruction can be found on https://developer.android.com/studio/install .
2. Follow the guide, and install Android Studio on your computer, **Note: You need to make sure that gradle is installed, and added to path.**
3. Now, it's the time to work with this project. 
   1. Download the latest release of this project
     * If you prefer to download directly from browser, go to this link: https://github.com/Aurorum-Studio/flarum-app/releases
     * If you prefer to download with git, run ```git clone https://github.com/Aurorum-Studio/flarum-app.git```
   2. Customize your application. (For more instruction of the structure of this project, read this doc.)
     * To change the name of the application, 
     > Browse to (relative path) /app/src/main/res/values/strings.xml, and change the "My Flarum" on the second line "<string name="app_name">My Flarum</string>", into the app name you want.
     > ![图片](https://user-images.githubusercontent.com/88573201/221529286-5cf82de0-681f-4185-9041-afed316b7d2f.png)
     * To change the name of the package,
     > go to the MainActivity.java file, and follow the following images
     > ![图片](https://user-images.githubusercontent.com/88573201/221529922-bed060e2-ceee-484d-85a9-f66fcd13bccb.png)
     > ![图片](https://user-images.githubusercontent.com/88573201/221530192-d17d7a48-25ba-4bb4-abb7-7a30ba665f65.png)
     > #### **!!!Warning!!!: If your previous package name is like shown in the image, including strings like "www", or "com", DO NOT change the package name in this way, you should change it in other ways, while that would take a lot of work. Thus, DO NOT use names contain these strings unless it's your last time to change your package name. If you download this project directly from official release, you WOULD NOT recieve a project with those strings.**
     > ![图片](https://user-images.githubusercontent.com/88573201/221531896-38ca748d-0cdb-4cc0-a0e0-cd7814dfa702.png)
     > And, that's done.
     * To change the icon of your application:
     > ![图片](https://user-images.githubusercontent.com/88573201/221532414-bb67d151-b04a-443b-bdf8-d9c10232dacd.png)
     > ![图片](https://user-images.githubusercontent.com/88573201/221532860-f6d4b1ea-9f2e-4e1f-8e45-5d14aea53da2.png)

4. You have already done most of your DIY work, for more DIY-able details, go to this doc. （Documentation on building, link would be avaliable after it's built.)
5. Now, it's time to build this project into an application.
    > ![图片](https://user-images.githubusercontent.com/88573201/221533741-00b7f65b-78a9-4763-a56f-18be33605d8a.png)
    > Click make project, and your app is built, with the path given by Android Studio.

## Todo list (It's very welcomed to make the todo list become true before me, and please make a pull request if you did.):
1. Build a version made with firefox (gecko), to make sure users with poor webview support can use this app.
2. Add a offline cache read feature, to allow users use the app offline.
3. Make this Readme file better.
4. Optimize the appearance of this app:
   * Add a better-looking loading
   * Add a better header.
5. Make a native Android app for flarum. (This would be a lot of work.)

## At last, if you like this project, please star it. It's also very welcomed to contribute to this project through pull request, or issue, discussions. If you want to support me, please go to https://dl.aurorum.co , and click the ads in a discussion. (I only set a little ads, sorry for make it a little hard to find.

Here are some ways you can get support:

Discussions: 
* HhiLan Support Tag: https://www.hhilan.com/d/131-aurorum-studioflarum-app （Sorry for using a photography site for support, but the domain I always use(the second option) is blocked in China, and I may not get notification when you need help using that domain)
* Aurorum Dev Site: https://dev.aurorum.co/d/91-aurorum-studioflarum-app (Blocked in China)
* Flarum Discussion: https://discuss.flarum.org/d/32467-unofficial-flarum-android-app

Issues: Github: https://github.com/Aurorum-Studio/flarum-app/issues
     
     
  
     

