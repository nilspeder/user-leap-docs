# Android SDK Updates

We adhere to [Semver](https://semver.org/) for versioning our SDKs so upgrading between major versions \(e.g. 1.0.1-&gt; 1.1.0\) should not present any breaking changes.

Note: 1.2.1 is the same as 2.0.0, we've bumped the major version to signify that versions below 1.2.1 will be disabled/deprecated by Feb 12, 2021

### Upgrading from 1.x.x to 2.x.x

* `UserLeap.visitorIdentifier` which returns `Int?` will always return null for new visitors. Please use the new `UserLeap.visitorIdentifierString` which returns `String?`

Please follow the [Android Installation Guide](https://docs.userleap.com/installation/android-sdk) to upgrade your UserLeap SDK to the [latest release listed](https://bintray.com/userleap/userleap-android-sdk/userleap-android-sdk)



