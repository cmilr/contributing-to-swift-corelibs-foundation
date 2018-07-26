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
// NOTE: see end of readme for the above two aliases, plus others I find useful
```
Finally:

* CD into **swift-source/swift-corelibs-foundation/**
* Open **Foundation.xcworkspace**.
* Build the **SwiftFoundation** target (this builds CoreFoundation and Foundation.)
* Run the **TestFoundation** target (this builds CoreFoundation, Foundation, XCTest, and TestFoundation, then runs the tests.)

```sh
alias cdswift="cd /Users/cmilr/Dev/Repos/swift-source/swift"
alias selectxcode="sudo xcode-select -switch /Applications/Xcode.app/Contents/Developer"
alias selectbeta="sudo xcode-select -switch /Applications/Xcode-beta.app/Contents/Developer"
alias swifttest="${LLVM_SOURCE_ROOT}/utils/lit/lit.py -sv ${SWIFT_BUILD_DIR}/test-macosx-x86_64"
alias swiftvaltest="${LLVM_SOURCE_ROOT}/utils/lit/lit.py -sv ${SWIFT_BUILD_DIR}/validation-test-macosx-x86_64"
alias updateswift="selectbeta; cdswift; utils/update-checkout --clone-with-ssh"
alias buildswift="selectbeta; cdswift; utils/build-script --release-debuginfo"
```

