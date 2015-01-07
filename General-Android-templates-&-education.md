### Android libraries
There are all the libraries we use in the app today: [libraries](https://github.com/nstevens/androidguide/wiki/Libraries)

### Build.gradle
We use [gradle](http://developer.android.com/sdk/installing/studio-build.html) as our build system, the default with Android Studio.  Here are the customizations we've made to our `build.gradle` file:

Within `android {}`:

* We compile with Java 1.7:
```java
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_7
        targetCompatibility JavaVersion.VERSION_1_7
    }
```

* We use build types to [zipalign](http://developer.android.com/tools/help/zipalign.html) release builds. This has a bigger impact if you have a large app with more images
```java
    buildTypes {
        release {
            zipAlign true
        }

        debug {
        }
    }
```

* We use [product flavors](http://tulipemoutarde.be/2013/10/06/gradle-build-variants-for-your-android-project.html) to easily switch between pointing to our own dogfood and production servers:
```java
    productFlavors {
        prod {}

        stage {}
    }
```

### Design templates
* Google official Phone & Tablet stencils, Photoshop mocks, Action Bar Icons, wear materials, style guide and Color pallete - [link](https://developer.android.com/design/downloads/index.html)
* Sketch Material Design template - [link](http://www.sketchappsources.com/free-source/653-android-l-tablet-ui-template.html)

### General education and other guides
* Good 'designing for android' intro - [slideshare link](http://www.slideshare.net/yiibu/designing-for-diversity-how-to-stop-worrying-and-embrace-the-android-revolution/86)
* Tumblr of 'beautifully designed' android apps - [link](http://androidniceties.tumblr.com/)
* "Building the Prismatic Android Loader Animation" by [Steven Schafer](https://twitter.com/stevenschafer) - [link](https://medium.com/@stevenschafer/building-the-prismatic-android-loader-animation-989bd7b30dca)
* Great blog about Android UI patterns - [link](http://www.androiduipatterns.com/) 
* Mobile UI patterns blog that has good Android examples - [link](http://www.mobile-patterns.com/)
* Official Android Material UI guidelines - [link](http://www.google.com/design/spec/material-design)
* Android stencils - [link](http://developer.android.com/design/downloads/index.html)
* Custom Android libraries we could use - [link](http://www.androidviews.net/)
* Android developer blog - [link](http://android-developers.blogspot.com/)
* Vogella's Dev Tutorials - [link](http://www.vogella.com/tutorials/android.html)