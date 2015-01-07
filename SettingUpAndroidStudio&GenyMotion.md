## Download
* Download the latest [Android Studio](http://developer.android.com/sdk/installing/studio.html)
* Download the latest [Virtual Box for Mac](https://www.virtualbox.org/wiki/Downloads)
* Register and download latest [Genymotion](https://shop.genymotion.com/index.php?controller=order-opc)

## Genymotion
Genymotion is a fast Android emulator for testing your app on your computer.

**1.** Install VirtualBox with the default settings

**2.** Install Genymotion by copying over both icons to your Applications folder.

**3.** Open up Genymotion and 'Add' a new virtual device.

You can add any VM you want, so long as it matches the Android versions your app supports.  We chose to support Android 4.0.3 (API 15) and above so a lot of people currently have the 'Google Nexus 5 - 4.4.2 - API 19 - 1080x1920' image.

After it's downloaded, you can start the VM by selecting it and pressing 'Play'

## Android Studio
**1.** Copy over the Android Studio icon to Applications

**2.** Open up Android Studio.  In the initial 'Welcome to Android Studio' window, click 'Android Studio' on the mac menu bar and click 'Check for updates'.  Keep doing this until you're up to date.

**3.** Then, still in the initial 'Welcome to Android Studio' window, click 'Configure' -> 'SDK Manager'

### SDK Manager

By the end, you want to have the packages based on the image below.  You'll have to probably go through multiple rounds of selecting checkboxes to install/remove certain packages until you're happy.  

Between rounds, you may have to quit SDK Manager and restart it from the 'Welcome to Android Studio' window.  Also if you ever see an error on a package after downloading it, quit and restart the SDK Manager.  Finally, quit and reopen it at the end to verify that the right packages are there and you're done.

![](http://i.imgur.com/QqsBUUU.png)
[Link to the image](http://i.imgur.com/QqsBUUU.png) for a bigger view

### Importing the project

Assuming you are already [setup with git and github](SettingUpGit.md), first: clone the repo from your terminal:

````
cd ~/
git clone git@github.com:ADDRESS.git
```

If you've previously cloned the repo, make sure you're up to date with the latest

```
cd ~/android
git checkout master
git pull origin master
```

Then, in the initial Android Studio window, select 'Import Project' and select the base ~/android folder:

![](http://i.imgur.com/UFyTJVF.png)

Then you should be good to go!