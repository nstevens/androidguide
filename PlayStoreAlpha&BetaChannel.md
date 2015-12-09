### Intro from the Google Documentation

> Google Play Developer Console lets you select your groups of testers either through creating a Google Group (what we use) or Google+. Add a Google+ Community URL or a Google Groups email address to the Developer Console to select your test group (already done). The Developer Console will give you a URL that you need to give to the users (below). They’ll need to go to the URL, which will explain what it means to be a tester and they can opt in. Then they can click a link from that page to download the app in the Play Store and the right updates!

[Source](https://support.google.com/googleplay/android-developer/answer/3131213)

### Our three channels
At Prismatic, we have an alpha and beta Google Groups for the respective channels.  Everyone is a user in @getprismatic.com is automatically added to the Alpha.  The permissions of both groups are modified so only @getprismatic.com users can send emails to the groups, see the email list and add people.

* **Alpha:** We use this channel just for the company dogfooding.  We push a new alpha every Wednesday & Friday at minimum. If you have a separate personal email attached to your Play Store account, you'll need to add it here.
* **Beta:** external, invited users. We get a great amount of feedback and bug reports from ~1k invited users.  We push Friday's alpha to the beta channel every Tuesday
* **Production:** (everyone), available in the Play Store

### How to invite a user.
Invite the user to the Google Group and then send them your custom opt-in link.  For example: https://play.google.com/apps/testing/app.package.name

### A script to automate publishing to the Play Store
We use [this script](https://github.com/googlesamples/android-play-publisher-api) to automatically push a new apk to the alpha channel (by default). There's also a [jenkins equivalent](https://wiki.jenkins-ci.org/display/JENKINS/Google+Play+Android+Publisher+Plugin).

### Final note on the `versionCode`
If the `versionCode` is higher on Production than an Alpha or Beta build, those users will automatically get the Production Build and later update to the Alpha or Beta again if a new apk overtakes the production `versionCode` again.

More details on removing users, doing production staged rollouts, etc are [here](https://support.google.com/googleplay/android-developer/answer/3131213?hl=en)

---
[Wiki home](https://github.com/nstevens/androidguide/) | [Android app](http://play.google.com/store/apps/details?id=com.Prismatic.android) | [Prismatic Github](http://github.com/Prismatic) | [Prismatic](http://getprismatic.com) | [My email](mailto:nick@eyesturnedskywards.com) | [My Twitter](http://twitter.com/njs)