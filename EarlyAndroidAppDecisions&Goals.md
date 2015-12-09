### Our app will support Android 4.0.3 (API 15) and above
This equates to ~96% of internet connected Android devices as of November, 2014.  As of December, 2015, supporting Android 4.2+ (API 17) gets you ~83% ([source](https://developer.android.com/about/dashboards/index.html))

Android has gone through a lot of rapid change with each of its 10 major versions. [Comprehensive ArsTechnica 'History of Android'](http://arstechnica.com/gadgets/2014/06/building-android-a-40000-word-history-of-googles-mobile-os/)

The latest version is Android 6.0, released in October, 2015.  With Android 4.0, Google made a concrete push to standardize widely used techniques, libraries and UI elements.  Writing an app for pre 4.0 means restricting to older APIs, a more limited test suite and often writing more code.  Starting an app now and concretely not supporting older versions will save us a lot of implementation and compatibility/QA time.

### We prefer stock and widely supported libraries over 'rolling our own' whenever possible.
Since Android is not owned by one device company, every top manufacturer has tried to differentiate themselves from others by writing custom ‘wrappers,’ launchers, etc on top of the Android Open Source Platform (AOSP).  This means that two Android users with devices made by different manufacturers can have wildly different experiences.  On top of that, service providers (Verizon, Sprint, etc) add their own apps and experiences to differentiate themselves as well.

**For design:** this means that overly optimizing for certain devices, even top devices, is a mistake.  We need to understand what UI and visual patterns are global or device specific and use that information appropriately.

**For both design & engineering:** that means that when you 'roll your own,' you often spend a majority of your time ensuring that it works with the range of devices, screens, apps, etc that people have on their phone.  Instead, using supported stock components means that this strain is largely abstracted away from us.  

This does not mean we can't be creative.  There are so many options and customizations even within stock & widely supported libraries.

[These](Libraries.md) are the libraries the Prismatic Android app uses today.

### We are creative and take advantage of the unique attributes of Android
Unique Android attributes include global share intents for info coming into and leaving our app, back button and navigation between apps, rich notifications, fragments and scalable design across screen sizes and densities. [@Stammy](http://twitter.com/stammy) has a good overview of unique attributes [here](http://paulstamatiou.com/android-is-better/).

### All designs are relative and focus on fragment reuse
‘Relative’ so that they can fit with the range of screen size and densities ([details](http://developer.android.com/guide/practices/screens_support.html)).

Fragment reuse means we can stack views on top of each other on a phone but potentially resize and put different fragments together on larger tablets without having to code custom layouts ([Android guide](http://developer.android.com/training/basics/fragments/index.html))

### Using the Play Store for alpha & beta testing
At Prismatic, we use the Play Store to internally dog food the latest builds (alpha channel) and test newly implemented ideas with a handful of invited beta testers (beta channel) before rolling the changes to everyone (prod channel).

Instructions to set up your own channels are [here](PlayStoreAlpha&BetaChannel).

---
[Wiki home](https://github.com/nstevens/androidguide/) | [Android app](http://play.google.com/store/apps/details?id=com.Prismatic.android) | [Prismatic Github](http://github.com/Prismatic) | [Prismatic](http://getprismatic.com) | [My email](mailto:nick@eyesturnedskywards.com) | [My Twitter](http://twitter.com/njs)
