# iOS SDK Updates

We adhere to [Semver](https://semver.org/) for versioning our SDKs so upgrading between major versions \(e.g. 2.0.0 -&gt; 2.1.0 or 3.1.0 &gt; 3.2.1\) should not present any breaking changes.

### Upgrading from 3.1.1 to 3.2.0/4.x.x

Note: 3.2.0 is the same as 4.0.0, we've bumped the major version to signify that versions below 3.2.0 will be disabled/deprecated by Feb 12, 2021

Changes:

* `UserLeap.shared.visitorIdentifier` which returns `NSNumber?` will always return `nil` for new visitors. Please use the new `UserLeap.shared.visitorIdentifierString` which returns `String?`

### Upgrading from 2.x.x to 3.1.1

Please be aware of 2 breaking changes in this upgrade:

#### Visitor Identifier Getter

To better support the Objective-C runtime, we have changed the return type of `UserLeap.shared.visitorIdentifier` from `Int?` to `NSNumber?`. If you are using `visitorIdentifier` in your codebase and expect it to be an `Int`, please be sure to call `intValue` on that value if it is non-nil.

#### UserLeap init\(\) calls are officially deprecated

As with all versions of this SDK, please use the provided single `UserLeap.shared` instead.

### How to upgrade

#### Cocoapods

Locate your `Podfile` that has declared `UserLeapKit` as a dependency and update the version number to the [latest release listed](https://github.com/UserLeap/userleap-ios-sdk-releases/releases) \(e.g. `pod 'UserLeapKit', '~> 3.2.0'` \) and then run `pod install`

#### Carthage

Simply run `carthage update` in the same directory as your `Cartfile`

#### Manual

If you linked the `UserLeapKit` framework manually through Xcode, please download the [latest release listed](https://github.com/UserLeap/userleap-ios-sdk-releases/releases) and follow the instructions for [Installing Manually](https://docs.userleap.com/installation/ios-sdk#installing-manually)

