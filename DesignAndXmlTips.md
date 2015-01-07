### dp & sp
([from stackoverflow](http://stackoverflow.com/a/2025541/2561578))  

**dp - Density-independent Pixels** - an abstract unit that is based on the physical density of the screen. These units are relative to a 160 dpi screen, so one dp is one pixel on a 160 dpi screen. The ratio of dp-to-pixel will change with the screen density, but not necessarily in direct proportion (see *3). Note: The compiler accepts both "dip" and "dp", though "dp" is more consistent with "sp".  

**sp - Scale-independent Pixels** - this is like the dp unit, but it is also scaled by the user's font size preference. It is recommend you use this unit when specifying font sizes, so they will be adjusted for both the screen density and user's preference.  

*1 Android documentation is pretty adamant about using sp with text, and it makes sense for things like full view body text.  I wonder if it's smart to use it for things that we truncate, especially to one line. Maybe a user with a large font preference would only get a couple words?  Do we maybe allow more than one line (and instead limit by number of words or something)? I don't know.  

*2 never use anything but dp & sp unless you absolutely have to.    

*3 Another good note: "The scaling that occurs for these depends not on the devices real density (dpi) but on which "bucket" of densities it falls into (see below). This can cause some problems handling screens that are significantly different but get bucketed the same.”

![](http://i.imgur.com/LkBSmEE.png)

### Generating assets
If you're generating an actual 'drawable' (png, jpg, etc) from sketch: you need to generate a couple different sizes for the range of density buckets  

luckily there's a [sketch plugin](https://github.com/pixi-stix/sketch-mobile-assets  ) & [photoshop plugin](http://www.cutandslice.me/) that will do exactly that for you!

If you want to specifically generate app icon in multiple sizes: [link](http://romannurik.github.io/AndroidAssetStudio/icons-launcher.html)

If you want to compare a specific pixel measurement in one DPI to another, there's a [handy calculator](http://jennift.com/dpical.html)

Longer guide about all this: [link](http://developer.android.com/training/multiscreen/screendensities.html)

### User facing strings
We put **all** the user facing strings (or messages) in the `res/values/strings.xml` file.  Having it in one file (instead of distributed in the code) makes it easier to make changes and also translate our app into other languages.

A key is to never subdivide strings into multiple parts:

> After reading that part about localized format strings, you may be tempted to take a clever, DRY approach by creating reusable grammar templates like `"{Noun} {Verb} {Noun}", and localizing each word individually...

> **DON'T.** This cannot be stressed enough: don't subdivide localized strings. Context will be lost, grammatical constructions will be awkward and unidiomatic, verbs will be incorrectly conjugated, and you'll have missed the point entirely—taking great effort to make something worse than if you hadn't bothered in the first place.

(advice from [NSHipster - No Madlibs section](http://nshipster.com/nslocalizedstring/))

## Right to left language support
In XML, xxleft == xxstart and xxright ==xxend  

So, for example: `android:paddingLeft` is the same as `android:paddingStart`.  **Whenever you have one, you should have the other and both should be set to the same value.**

The reason to have both is to support translation (and specifically right to left languages hence the 'start' and 'end') while also supporting older android versions that look for 'left' and 'right'.  

Reasons:

![](http://i.imgur.com/b0ogonl.png)

Full details in [this blogpost](http://android-developers.blogspot.com/2013/03/native-rtl-support-in-android-42.html)