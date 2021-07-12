# Adobe Experience Platform - Places extension for iOS

[![Cocoapods](https://img.shields.io/cocoapods/v/AEPPlaces.svg?color=orange&label=AEPPlaces&logo=apple&logoColor=white)](https://cocoapods.org/pods/AEPPlaces)
[![SPM](https://img.shields.io/badge/SPM-Supported-orange.svg?logo=apple&logoColor=white)](https://swift.org/package-manager/)
[![CircleCI](https://img.shields.io/circleci/project/github/adobe/aepsdk-places-ios/main.svg?logo=circleci)](https://circleci.com/gh/adobe/workflows/aepsdk-places-ios)
[![Code Coverage](https://img.shields.io/codecov/c/github/adobe/aepsdk-places-ios/main.svg?logo=codecov)](https://codecov.io/gh/adobe/aepsdk-places-ios/branch/main)

## About this project

Adobe Experience Platform Places Extension is an extension for the [Adobe Experience Platform Swift SDK](https://github.com/adobe/aepsdk-core-ios).

The AEPPlaces extension allows you to track geolocation events as defined in the Adobe Places UI and in Adobe Launch rules.

## Requirements
- Xcode 11.x
- Swift 5.1 or newer

## Installation

### Binaries

To generate `AEPPlaces.xcframework`, run the following command from the root directory:

```
make archive
```

This will generate an XCFramework under the `build` folder. Drag and drop `AEPPlaces.xcframework` to your app target.

### [CocoaPods](https://guides.cocoapods.org/using/using-cocoapods.html)

```ruby
# Podfile
use_frameworks!

target 'YOUR_TARGET_NAME' do
      pod 'AEPPlaces'
end
```

### [Swift Package Manager](https://github.com/apple/swift-package-manager)

To add the AEPPlaces Package to your application, from the Xcode menu select:

`File > Swift Packages > Add Package Dependency...`

Enter the URL for the AEPPlaces package repository: `https://github.com/adobe/aepsdk-places-ios.git`.

Alternatively, if your project has a `Package.swift` file, you can add AEPPlaces directly to your dependencies:

```
dependencies: [
    .package(url: "https://github.com/adobe/aepsdk-places-ios.git", .upToNextMajor(from: "3.0.0"))
],
targets: [
    .target(name: "YourTarget",
            dependencies: ["AEPPlaces"],
            path: "your/path")
]
```

## Documentation
Additional documentation for configuration and SDK usage can be found under the [Documentation](Documentation/README.md) directory.

## PlacesTestApp & PlacesTestApp_objc
Two sample apps are provided (one each for Swift and Objective-c) which demonstrate retrieving nearby Points of Interest and triggering region events. Their targets are in `AEPPlaces.xcodeproj`, runnable in `AEPPlaces.xcworkspace`. Sample app source code can be found in the `TestApps` directory.

## Contributing
Looking to contribute to this project? Please review our [Contributing guidelines](.github/CONTRIBUTING.md) prior to opening a pull request.

We look forward to working with you!

## Licensing
This project is licensed under the Apache V2 License. See [LICENSE](LICENSE) for more information.
