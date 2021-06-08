# Android SDK Installation

Official Android SDK for UserLeap \([Releases](https://search.maven.org/artifact/com.userleap/userleap-android-sdk)\)

This SDK is designed to work with Android SDK 21 \(Android Lollipop, OS 5.0\) and above.

If using minSdk below 21, you can override the library in your main AndroidManifest.

```markup
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
  package="com.myapp"
    xmlns:tools="http://schemas.android.com/tools">

    <uses-sdk tools:overrideLibrary="com.userleap" />
    ....
```

Make sure to to check the [OS system version](https://developer.android.com/training/basics/supporting-devices/platforms#version-codes) before calling UserLeap.

```java
if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.LOLLIPOP) {
    UserLeap.configure(context, "YOUR_ENVIRONMENT_ID")
}
```

## Gradle

You can install the UserLeap SDK via [maven central](https://search.maven.org/artifact/com.userleap/userleap-android-sdk).

```groovy
dependencies {
    implementation 'com.userleap:userleap-android-sdk:2.2.0'
}
```

Add Java 8 support to your project \(if not added already\)

```groovy
android {
  ...
  compileOptions {
    sourceCompatibility JavaVersion.VERSION_1_8
    targetCompatibility JavaVersion.VERSION_1_8
  }
  // For Kotlin projects
  kotlinOptions {
    jvmTarget = "1.8"
  }
}
```

## Dependencies

* [Kotlin](https://developer.android.com/kotlin) \(1.3.72\)
* [Gradle](https://developer.android.com/studio/releases/gradle-plugin) \(4.0.0\)
* [Android X](https://developer.android.com/jetpack/androidx)
* [Java 8](https://developer.android.com/studio/write/java8-support)
* [Material Components](https://github.com/material-components/material-components-android) \(1.2.0-beta01\)- themed design components for surveys
* [ConstraintLayout](https://developer.android.com/reference/androidx/constraintlayout/widget/ConstraintLayout) \(1.1.3\) - flat view hierarchies for surveys
* [Retrofit \(2.9.0\) and Moshi](https://square.github.io/retrofit/) \(1.9.3\) - sending/receiving events and surveys
* [Okhttp](https://square.github.io/okhttp/) \(4.7.2\) - Networking library
* [Coroutines](https://developer.android.com/kotlin/coroutines) \(1.3.7\) - asynchronous support
* [WorkManager](https://developer.android.com/jetpack/androidx/releases/work) \(2.3.4\)- retry support for events and survey answers
* [Security](https://developer.android.com/jetpack/androidx/releases/security) \(1.0.0-beta01\) - encrypt sensitive data
* [Timber](https://github.com/JakeWharton/timber) \(4.7.1\) - locally and remotely log errors
* [Espresso Idling Resource](https://developer.android.com/training/testing/espresso/idling-resource) - UI testing

## Permissions

These permissions are automatically merged into your app Manifest.

* [INTERNET](https://developer.android.com/reference/android/Manifest.permission.html#INTERNET) - send and receive events and surveys

## **App size impact**

The UserLeap SDK AAR size is **373 KB**.

The impact to an Android App Bundle is **1.2 MB**. Note: The UserLeap SDK uses the common dependencies listed above. The actual size impact will be smaller if these dependencies are already used by the app. 

**Methodology**: Build a ProGuarded release Android App Bundle in Android Studio with an Empty Activity project. Then compare size after adding the UserLeap SDK.

