[![Twitter](https://img.shields.io/badge/Twitter-@PhilippJahoda-blue.svg?style=flat)](http://twitter.com/philippjahoda)
[![Twitter](https://img.shields.io/badge/Twitter-@mpandroidchart-blue.svg?style=flat)](http://twitter.com/mpandroidchart)
[![Release](https://img.shields.io/github/release/PhilJay/MPAndroidChart-Realm.svg?label=maven central)](https://jitpack.io/#PhilJay/MPAndroidChart-Realm)      [![API](https://img.shields.io/badge/API-16%2B-green.svg?style=flat)](https://android-arsenal.com/api?level=16)

![alt tag](https://raw.github.com/PhilJay/MPAndroidChart-Realm/master/design/feature_graphic.png)

This repository contains all [Realm.io](http://realm.io) related features of the [MPAndroidChart](https://github.com/PhilJay/MPAndroidChart) library based on **Realm v1.1.0** release.

# Getting Started

 - To use this library, add the following to your project level `build.gradle`:
```gradle
allprojects {
	repositories {
		maven { url "https://jitpack.io" }
	}
}
```
 - Add this to your app `build.gradle`:
```gradle
dependencies {
	compile 'com.github.PhilJay:MPAndroidChart-Realm:v1.1.0@aar'
}
```

The MPAndroidChart-Realm dependency **does not include** the latest MPAndroidChart release, so you have to add the dependency to [MPAndroidChart](https://github.com/PhilJay/MPAndroidChart#usage) as well.

# Tutorial

[Here](https://github.com/PhilJay/MPAndroidChart-Realm/wiki/Realm.io-database-integration), you can find a full guide on how to plot data from Realm.io database with MPAndroidChart from scratch.
