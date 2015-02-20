## Our favorite Android libraries
Below is a list of all the Android libraries we currently use in the [Prismatic Android app](http://play.google.com/store/apps/details?id=com.Prismatic.android).

If you have any questions about how we use them or know of specific libraries we should check out: just shoot us an email at feedback+android@getprismatic.com

* [**Picasso**](http://square.github.io/picasso/) - A powerful image downloading and caching library for Android 
* [**Retrofit**](http://square.github.io/retrofit/) - Type-safe REST client for Android and Java by Square, Inc. 
    * Handy JSON to Java Objects converter: [JSONSchema2Pojo](http://www.jsonschema2pojo.org/)
* [**RxAndroid**](https://github.com/ReactiveX/RxAndroid) - Reactive Extensions for the JVM – a library for composing asynchronous and event-based programs using observable sequences for the Java VM. 
* [**Dagger**](https://github.com/square/dagger) - A fast dependency injector for Android and Java. 
    * Note: we still use [Dagger 1.2.2 from Square](https://github.com/square/dagger) but plan to upgrade to [Dagger 2.0 from Google](https://github.com/google/dagger) when it's officially released.
* [**Otto**](http://square.github.io/otto/) - An enhanced Guava-based event bus with emphasis on Android support.
    * [Dave](https://twitter.com/davegolland) wrote a [detailed post](http://blog.getprismatic.com/android-state-saving/) about how we manage app state with Dagger & Otto.
* [**Butterknife**](http://jakewharton.github.io/butterknife/) - View "injection" library for Android.
* [**Pager Sliding Tab**](https://github.com/astuetz/PagerSlidingTabStrip) - An interactive indicator to navigate between the different pages of a ViewPager
* [**Circle Image View**](https://github.com/hdodenhof/CircleImageView) - A circular ImageView for Android 
* [**Crashlytics**](http://try.crashlytics.com/sdk-android/) - crash reporting in real-­time. 
* [**Google Play Services**](https://developer.android.com/google/play-services/index.html ) - for the [Google Analytics SDK](https://developers.google.com/analytics/devguides/collection/android/v4/) & Google auth
    * With [Google Play Services 6.5](http://android-developers.blogspot.com/2014/12/google-play-services-and-dex-method.html), you can now select subsets of the entire Play Services packages to use depending on what APIs you need. Since our app only uses analytics and google auth, we only import `services-base` and `services-plus`, saving ~500 kb from our build size.
* [**Google Support Library v13**](https://developer.android.com/tools/support-library/features.html)
* [**Google App Compat Library v7**](https://developer.android.com/tools/support-library/features.html#v7-appcompat) - to support select Material Design elements in earlier versions of Android. [guide](MaterialDesign.md)

We haven't settled on a final testing suite. Right now we're trialing [mockito](https://code.google.com/p/mockito/), [roboelectric](http://robolectric.org/) and [appium](http://appium.io/) with Clojure.  [Let us know](mailto:nick@getprismatic.com) if you have tips!

---
[Wiki home](https://github.com/nstevens/androidguide/) | [Android app](http://play.google.com/store/apps/details?id=com.Prismatic.android) | [Prismatic Github](http://github.com/Prismatic) | [Prismatic](http://getprismatic.com) | [My email](mailto:nick@getprismatic.com) | [My Twitter](http://twitter.com/njs)