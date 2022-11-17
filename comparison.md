---
name: Comparison
---

Comparison of App Fair with other app distribution networks
===========================================================

# F-Droid

[F-Droid](https://en.wikipedia.org/wiki/F-Droid) is an app store and software repository for Android, serving a similar function to the Google Play store. The main repository, hosted by the project, contains only free and open source apps. Applications can be browsed, downloaded and installed from the F-Droid website or client app without the need to register for an account. "Anti-Features" such as advertising, user tracking, or dependence on non-free software are flagged in app descriptions.

The following table attempts to summarize some of the similarities and differences between the App Fair and F-Droid[^0]. 

## Comparison of F-Droid and the App Fair

### App Technology

| Tech  | F-Droid | The App Fair |
| --- | --- | --- |
| Platforms | Google Android | Apple iPhone, iPad, macOS |
| Primary App Dev Languages | Java, Kotlin, + | Swift, Objective-C, C |
| App UI Framework | Any Android | SwiftUI and UIKit |
| Catalog Input Metadata | YAML | YAML |
| Catalog Output Metadata | JSON[^8] | JSON[^9] |
| Catalog Transmission | HTTPS | HTTPS |

### Build System Technology

| Tech  | F-Droid | The App Fair |
| --- | --- | --- |
| Platform | Debian, Ubuntu, etc. | macOS |
| Build Automation | Mostly | Fully |
| Build Manager | Python[^1] | Swift |
| Build System | Gradle, Ant, + | Swift Package Manager, Xcode |
| Build Host | Debian, Ubuntu, + (various locations) | macOS 12 (GitHub runner hosts, various locations) |
| Catalog Metadata | YAML | JSON |
| App Signing | Manual(?) | Automatic |
| Build Initiation | Semi(?) automatic | Automatic (GH action triggered by PR) |
| Build Automation | Mostly(?) automatic | Fully automatic |
| Distribution Channels | F-Droid, G-Droid[^2], + | App Store, AltStore[^3], App Fair |
| Artifacts | .apk (F-Droid build) | .ipa (developer's GitHub release, re-signed) |
| Catalog Indexing | Periodic(?) | Hourly GitHub Action |

### Gatekeeping

| Tech  | F-Droid | The App Fair |
| --- | --- | --- |
| Platform | Android | iPhone |
| App Approval | Manual | Semi automatic |
| Build Replication | Optional | Required |
| Remediation | Proactive, Retroactive | Retroactive |
| App Signing Key | F-Droid Project (manual) | App Fair Project (automatic) |
| Open Source | Required (transitive) | Required (transitive) |
| License Requirement | OSS (transitive) | AGPL+ (non-transitive), OSS (transitive) |
| Code Scanning | SUSS[^6] | VirusTotal, GitHub |

### App Behavior

| Tech  | F-Droid | The App Fair |
| --- | --- | --- |
| Sandboxing | Required | Required |
| Device Rooting/Jailbreaking | Unnecessary | Unnecessary |
| Device Service Access | Play Services Unavailable | iCloud Semi-available[^7] |


### Policies

Key:
  - :green_square: Required
  - :green_circle: Encouraged
  - :yellow_circle: Neutral
  - :red_circle: Discouraged
  - :red_square: Forbidden

| Tech  | F-Droid[^4][^5] | The App Fair |
| --- | --- | --- |
| Platform | Android | iPhone, iPad, macOS |
| Source Code Availability | :green_square: | :green_square: |
| Ongoing Maintenance | :green_square: | :green_square: |
| Permission/Entitlement Disclosure | :green_square: | :green_square: |
| Transitive Source Code Availability | :green_square: | :green_square: |
| Tagged Releases | :green_circle: | :green_square: |
| Publicly Accessible Version Control System | :green_square: | :green_square: |
| Non-Free Dependencies | :red_circle: | :red_square: |
| Tracking/analytics | :red_circle: | :red_square: |
| Advertisements | :red_circle: | :red_square: |
| Upstream Non-Free Source | :red_circle: | :red_square: |
| In-App Executable Binary Downloads | :red_square: | :red_square: |
| Non-Free Network Services | :red_circle: | :yellow_circle: |
| Non-Free Add-ons/Extensions | :red_circle: | :yellow_circle: |
| App Clones / Rebranded Forks | :red_circle: | :red_circle: |
| Cryptocurrency Apps | :yellow_circle: | :red_circle: |
| NSFW or Extreme Content | :red_circle: | :red_circle: |
| Trademark Infringement | :red_square: | :red_square: |


[^0]: Please help correct any errors, omissions, or outdated references to https://f-droid.org materials by submitting a [pull request](https://github.com/appfair/appfair.github.io/blob/main/comparison.md).
[^1]: https://gitlab.com/fdroid/fdroidserver
[^2]: https://f-droid.org/en/packages/org.gdroid.gdroid/
[^3]: https://altstore.io
[^4]: https://f-droid.org/en/docs/Inclusion_Policy/
[^5]: https://f-droid.org/en/docs/Anti-Features/
[^6]: Suspicious or Unwanted Software Signatures. https://fdroid.gitlab.io/fdroid-suss
[^7]: iCloud and other services are likely only to be available when apps are distributed through the official App Store. E.g., independently notarized macOS apps cannot use iCloud services.
[^8]: https://f-droid.org/repo/index-v2.json
[^9]: https://appfair.net/fairapps-ios.json

