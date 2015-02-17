# Introduction
[Prismatic](http://getprismatic.com) just released our first native Android app! Download it [**here**](https://play.google.com/store/apps/details?id=com.Prismatic.android).

This is the internal guide I wrote to motivate some early Android decisions and educate everyone on the platform.
This guide is intended for anyone from a new android engineer who just wants to write code as fast as possible, to designers who are interested in committing style changes or assets to the android repo.

Let us know if you have any feedback or additions! nick@getprismatic.com

# Summary
### [Getting setup](Setup.md)
* Get your computer & environment set up to commit code! This covers git, Android Studio and Genymotion setup: [guide](Setup.md)

### [Early Android App Decisions & Goals](EarlyAndroidAppDecisions&Goals.md)
* We've chosen to support all devices Android 4.0.3 (API 15) and above - [details](EarlyAndroidAppDecisions&Goals.md#our-app-will-support-android-403-api-15-and-above)
* We prefer stock and widely supported libraries over 'rolling our own' whenever possible - [details](EarlyAndroidAppDecisions&Goals.md#we-prefer-stock-and-widely-supported-libraries-over-rolling-our-own-whenever-possible)
* We are creative and take advantage of the unique attributes of Android and new ideas we want to implement. - [details](EarlyAndroidAppDecisions&Goals.md#we-are-creative-and-take-advantage-of-the-unique-attributes-of-android)
* All designs are relative and focus on fragment reuse - [details](EarlyAndroidAppDecisions&Goals.md#all-designs-are-relative-and-focus-on-fragment-reuse)
* We'll use the play store to beta test with real users as early as possible. - [how](EarlyAndroidAppDecisions&Goals.md#using-the-play-store-for-alpha--beta-testing)

### [General Android education & resources](GeneralAndroidTemplates&Education.md)
* **Android libraries:** These are all the libraries we use in the app today: [libraries](Libraries.md)
* **App State:** - Detailed post on how we manage client app state: [post](http://blog.getprismatic.com/android-state-saving/)
* **Using Gradle** - Here are some customizations we made to our gradle settings: [build.gradle](GeneralAndroidTemplates&Education.md#buildgradle)
* **Design resources:** fonts, colors, icons, stencils for sketch and photoshop. A guide to how we added animations to the app: [resources](GeneralAndroidTemplates&Education.md#design-templates)
* **General education** and other android resources: [education](GeneralAndroidTemplates&Education.md#general-education-and-other-guides)
* **Play Store:** scripts to automate publishing new builds to the Play Store: [from your computer](https://github.com/googlesamples/android-play-publisher-api), [jenkins](https://wiki.jenkins-ci.org/display/JENKINS/Google+Play+Android+Publisher+Plugin)
* **Intents:** a handy app to debug how your app handles [intents](http://developer.android.com/guide/components/intents-filters.html): [play store](https://play.google.com/store/apps/details?id=uk.co.ashtonbrsc.android.intentintercept&hl=en)

### [Design and xml tips](DesignAndXmlTips.md)
* **dp & sp:** remember to always use density independent pixels (dp) with all measurements and scale-independent pixels (sp) with fonts. dp is your friend but will still require specific testing, and there are tools for when you want to generate assets at multiple densities - [details](DesignAndXmlTips.md#dp--sp)
* **generating assets:** assets needs to be generated in multiple sizes for the different screen density buckets.  there are tools for doing it automatically from sketch & photoshop - [details](DesignAndXmlTips.md#generating-assets)
* **user facing strings:** they should all be in one file for easy editing and translation - [details](DesignAndXmlTips.md#user-facing-strings)
* **start & end vs left & right:** in xml, those two are the same thing(s) and should always have the same measurements.  They are specifically there to support right to left languages - [details](DesignAndXmlTips.md#right-to-left-language-support)

### Acknowledgements
Thank you to [Mohammad Almalkawi](https://twitter.com/moh), [Saud Khan](https://twitter.com/bidyut), [Ade Oshineye](https://plus.google.com/+AdeOshineye), [Paul Matthews](https://plus.google.com/+PaulMatthews86), [Ben Manes](https://github.com/ben-manes), and our [very astute beta tests](http://getprismatic.com/androidbetatesters) and the many authors of [these libraries](Libraries.md)! 

Let me know if you have any feedback or tips on [email](mailto:nick@getprismatic.com) or [Twitter](http://twitter.com/njs). More Prismatic open source available [here](http://github.com/Prismatic/).

---
[Wiki home](https://github.com/nstevens/androidguide/) | [Android app](http://play.google.com/store/apps/details?id=com.Prismatic.android) | [Prismatic Github](http://github.com/Prismatic) | [Prismatic](http://getprismatic.com) | [My email](mailto:nick@getprismatic.com) | [My Twitter](http://twitter.com/njs)
