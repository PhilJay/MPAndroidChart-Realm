[![Twitter](https://img.shields.io/badge/Twitter-@PhilippJahoda-blue.svg?style=flat)](http://twitter.com/philippjahoda)
[![Twitter](https://img.shields.io/badge/Twitter-@mpandroidchart-blue.svg?style=flat)](http://twitter.com/mpandroidchart)
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-MPAndroidChart--Realm-green.svg?style=true)](https://android-arsenal.com/details/1/3838)
[![Release](https://img.shields.io/github/release/PhilJay/MPAndroidChart-Realm.svg?style=flat)](https://jitpack.io/#PhilJay/MPAndroidChart-Realm)      [![API](https://img.shields.io/badge/API-16%2B-green.svg?style=flat)](https://android-arsenal.com/api?level=16)

![alt tag](https://raw.github.com/PhilJay/MPAndroidChart-Realm/master/design/feature_graphic.png)

This repository contains all [Realm.io](http://realm.io) related features of the [MPAndroidChart](https://github.com/PhilJay/MPAndroidChart) library based on **Realm v4.2.0** release.

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
	implementation 'com.github.PhilJay:MPAndroidChart-Realm:v3.0.3@aar'
	implementation 'com.github.PhilJay:MPAndroidChart:v3.0.3'
}
```

The MPAndroidChart-Realm dependency **does not include** the latest MPAndroidChart release, so you have to add the dependency to [MPAndroidChart](https://github.com/PhilJay/MPAndroidChart#usage) as well (as shown above). You also have to add the [Realm.io dependency](https://realm.io/docs/java/latest/#getting-started).

# Sample

Using [MPAndroidChart](https://github.com/PhilJay/MPAndroidChart) with [Realm.io](https://realm.io) is easier than you think.

```java
// get realm instance
Realm realm = Realm.getDefaultInstance();

// load your data from Realm.io database
RealmResults<YourData> results = realm.where(YourData.class).findAll();

// create a DataSet and specify fields, MPAndroidChart-Realm does the rest
RealmBarDataSet<YourData> dataSet = new RealmBarDataSet<YourData>(results, "xValue", "yValue");

// create a data object with the dataset 
BarData data = new BarData(dataSet);
chart.setData(data);
chart.invalidate(); // refresh
```

# Tutorial

[Here](https://github.com/PhilJay/MPAndroidChart-Realm/wiki/Realm.io-database-integration), you can find a full guide on how to plot data from Realm.io database with MPAndroidChart from scratch.
