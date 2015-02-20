Material Design was introduced by Google with Android 5.0 (lollipop).  

### Android 5.0 vs older phones
The full range of design elements are available for any phone running Android 5.0 or above: ~1.6% of devices as of February, 2015 ([source](https://developer.android.com/about/dashboards/index.html)).  While phones are upgrading, you can also support a select subset of elements on older devices via the [App Compat library](https://developer.android.com/tools/support-library/features.html#v7-appcompat), specifically:

>* [Material design styles](https://developer.android.com/training/material/theme.html) for some system widgets when you apply one of the `Theme.AppCompat` themes.
>* [Color palette theme attributes](https://developer.android.com/training/material/theme.html#ColorPalette) in the `Theme.AppCompat` themes.
>* The [RecyclerView](https://developer.android.com/reference/android/support/v7/widget/RecyclerView.html) widget to [display data collections](https://developer.android.com/training/material/lists-cards.html#RecyclerView).
>* The [CardView](https://developer.android.com/reference/android/support/v7/widget/CardView.html) widget to [create cards](https://developer.android.com/training/material/lists-cards.html#CardView).
>* The [Palette](https://developer.android.com/reference/android/support/v7/graphics/Palette.html) class to [extract prominent colors from images](https://developer.android.com/training/material/drawables.html#ColorExtract).

For backwards compatibility, [this very useful guide](https://developer.android.com/tools/support-library/features.html#v7-appcompat) goes through both upgrading old apps and adding App Compat supported material elements to new ones.  This [page](https://developer.android.com/training/material/compatibility.html) also has some useful tips like the reminder to set your `android:targetSdkVersion` to `21` in order to use the material design features on Android 5.0+ devices.

### Top Material Design resources
* Official Android Material UI guidelines - [link](http://www.google.com/design/spec/material-design)
* Mobile UI patterns blog that has good Android examples - [link](http://www.mobile-patterns.com/)
* AppCompat v21 — Material Design for Pre-Lollipop Devices! - [link](http://android-developers.blogspot.com/2014/10/appcompat-v21-material-design-for-pre.html)
* Implementing Material Design in your Android App (Android 5.0+) - [link](http://android-developers.blogspot.com/2014/10/implementing-material-design-in-your.html)
* Material Design on Android Checklist - [link](http://android-developers.blogspot.com/2014/10/material-design-on-android-checklist.html)

---
[Wiki home](https://github.com/nstevens/androidguide/) | [Android app](http://play.google.com/store/apps/details?id=com.Prismatic.android) | [Prismatic Github](http://github.com/Prismatic) | [Prismatic](http://getprismatic.com) | [My email](mailto:nick@getprismatic.com) | [My Twitter](http://twitter.com/njs)
