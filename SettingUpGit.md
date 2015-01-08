This basic introduction is intended for anyone getting started with git & github.

## What is git
* [Quick overview](http://rogerdudler.github.io/git-guide/)
* [More in depth](http://git-scm.com/book/en/Git-Basics)
* [Github's interactive tutorials](https://try.github.io/)

## Installing git
Follow steps 3, 4 and 5 of [this guide](http://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/)

## Connecting to our github repositories
If you're part of a larger organization, make sure someone with access rights has added you to the Github team so you can access any protected repositories

Set up your ssh keys following [this guide](https://help.github.com/articles/generating-ssh-keys)

Then, you should be able to clone a repository.  In general, it's best to have your local repositories live in your 'home' folder (represented by '~' in the terminal).  Your default home repository on a mac is `/Users/YOUR_USERNAME`.  To clone a repository into your home directory:

Open your terminal and type:
```
cd ~
git clone SSH_CLONE_URL
```

To get the appropriate address, go to the repository on github and grab the SSH clone URL

![](http://i.imgur.com/wIOihvg.png)

```
cd ~
git clone git@github.com:ADDRESS.git
```

Then you have the code on your computer!  

The best way to learn how to actually use git will be to pair with someone and ask questions the first time you want to make a change.

## Our git practices
If you plan to be regularly commiting code, please read the [Prismatic Git practices](https://github.com/Prismatic/eng-practices/blob/master/git/20140403-git.md). It covers our branching model, PR and commit rules, etc.

---
[Wiki home](https://github.com/nstevens/androidguide/) | [Android app](http://play.google.com/store/apps/details?id=com.Prismatic.android) | [Prismatic Github](http://github.com/Prismatic) | [Prismatic](http://getprismatic.com) | [My email](mailto:nick@getprismatic.com) | [My Twitter](http://twitter.com/njs)