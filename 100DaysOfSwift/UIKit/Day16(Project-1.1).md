# Day16 [Project]

## Begin to the IOS 

## Subjects

- Project Setup for UIKit
- Listing images with FileManager
- Designing our interface

## FileManager

A piece of code that tells where the contents are, although I find it very interesting

```swift
let fm = FileManager.default
let path = Bundle.main.resourcePath!
let items = try! fm.contentsOfDirectory(atPath: path)
```


