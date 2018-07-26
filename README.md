# Notes on: Swift CoreLibs Foundation

## macOS Development Setup

First, download and install:
* [The latest version of Xcode](https://developer.apple.com/download/)
* [The current version of the Swift toolchain](https://swift.org/download/#releases)

Then:
* Boot the latest version of **Xcode**.
* Enable the correct **toolchain** in **Xcode > Preferences > Components**.

Now:
```sh
$ updateswift
$ buildswift  // Preferably overnight
```
Finally:

* CD into **swift-source/swift-corelibs-foundation/**
* Open **Foundation.xcworkspace**.
* Build the **SwiftFoundation** target (this builds CoreFoundation and Foundation.)
* Run the **TestFoundation** target (this builds CoreFoundation, Foundation, XCTest, and TestFoundation, then runs the tests.)

> Note: If you see the name of the XCTest project file in red in the workspace, then Xcode cannot find the cloned XCTest repository. Make sure that it is located next to the swift-corelibs-foundation directory and has the name swift-corelibs-xctest.


