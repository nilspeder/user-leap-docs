# iOS SDK Installation

Official Releases of the UserLeap iOS SDK \([Releases](https://github.com/UserLeap/userleap-ios-sdk-releases/releases)\)

This SDK is designed to work with iOS 10.3 and above.

## Versioning

This SDK uses [Semantic Versioning 2.0.0](https://semver.org/).

You can find the latest release version [here](https://github.com/UserLeap/userleap-ios-sdk-releases/releases).

## Installation

There are three ways you can include UserLeap in your application:

### CocoaPods

The recommended way to acquire this Framework is via [CocoaPods](https://cocoapods.org/). Simply add the following statement to your Podfile, then run `pod install`:

```bash
pod 'UserLeapKit', '~>4.3.0'
```

Then run this command in the same directory that contains your Podfile

```bash
pod install
```

### Carthage

If you're using [Carthage](https://github.com/Carthage/Carthage), add the following statement to your Cartfile

```bash
binary "https://raw.githubusercontent.com/UserLeap/userleap-ios-sdk-releases/main/UserLeapKit.json"
```

Follow the [instructions](https://github.com/Carthage/Carthage#quick-start) to finish the installation.

### Installing manually

If you’re unable to use Cocoapods or Carthage, you can also install UserLeap manually. Download the latest framework as a zip from our [Releases](https://github.com/UserLeap/userleap-ios-sdk-releases/releases). Unzip the downloaded file and drag the UserLeap.framework folder into your project directory.

Open Xcode and select your project in the “Project Navigator” pane, select your app under “TARGETS”. In the “Frameworks, Libraries, and Embedded Content” section, press “+”, “Add Other…”, “Add Files…” and select the UserLeap.framework folder.

![](https://lh3.googleusercontent.com/Jh5t0nVJUlL7uPJwLbeayxmy57_f3y2S2aoaUwQnCZMicmBF8nJmB3Ld4TzlQsLINGbOjvWDeBjIDUxv10KUgjQdvWx7-EsxdVNJGKlf8aqm71nueXSSKkDsOfLYDmQGpBia96eC)

Be sure that UserLeap.framework is in your project settings “Framework Search Paths” or you Xcode will throw the “no such module UserLeap” error.

![](https://lh5.googleusercontent.com/ki8F-lJq1soDu4WZ8uBgp_T5PE1NWMog2ImBpfcgzP02Yd1JH-yypVWLBu6S4vsbYbQBr0mGMV5PSzUFxetB9mcyh66ODLbNolzbGXhOnh7vF6Jh3czDBjsaKlYw1MJEScOOp0id)

## **App size impact**

UserLeap only uses `Foundation`, `UIKit`, `SystemConfiguration`, and `CoreGraphics` with no third-party frameworks to provide the smallest disk footprint on your app binary.

The SDK size is **234 KB** compressed and **592 KB** uncompressed

Note: Compressed is equivalent to the additional size downloaded from the App Store, and uncompressed is the additional size on an iPhone after installation

**Methodology**: Created a fresh Xcode project with and without UserLeapKit.framework and used the App Size Report tool \([Apple docs](https://developer.apple.com/documentation/xcode/reducing_your_app_s_size#//apple_ref/doc/uid/DTS40014195-CH1-MEASURE)\)

