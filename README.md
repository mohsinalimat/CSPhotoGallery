# CSPhotoGallery

[![CI Status](http://img.shields.io/travis/chansim.youk/CSPhotoGallery.svg?style=flat)](https://travis-ci.org/chansim.youk/CSPhotoGallery)
[![Version](https://img.shields.io/cocoapods/v/CSPhotoGallery.svg?style=flat)](http://cocoapods.org/pods/CSPhotoGallery)
[![License](https://img.shields.io/cocoapods/l/CSPhotoGallery.svg?style=flat)](http://cocoapods.org/pods/CSPhotoGallery)
[![Platform](https://img.shields.io/cocoapods/p/CSPhotoGallery.svg?style=flat)](http://cocoapods.org/pods/CSPhotoGallery)

- This is very simple and light photo browser written swift. and also you can show images or videos.

![Sample Project](Example/CSPhotoGallery.gif)

Supports iOS 9.0+, Swift 3.0

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Requirements

## Installation

CSPhotoGallery is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "CSPhotoGallery"
```

## Usage

First Step  - `@import CSPhotoGallery` to your project 

Second Step - Add a delegate `CGPhotoGalleryDelegate` to your class & add two delegate methods 
```Swift
func getAssets(assets: [PHAsset]) {
  // if you implement this delegate function, you will receive assets
}

func dismiss() {
  //  Photo browser dismiss
  // ex)
  //  dismiss(animated: true) {
  //   do something
  //  }
}
```
Third Step - Present a CSPhotoGalleryViewController

```Swift
let vc = CSPhotoGalleryViewController.instance
vc.delegate = self
vc.CHECK_MAX_COUNT = 20
vc.horizontalCount = 3
vc.mediaType = .image //  or .video
present(vc, animated: true)
```
And you can customize ui design
```Swift
let designManager = CSPhotoDesignManager.instance
designManager.photoDetailBackButtonImage
designManager.photoDetailOKButtonTitle
designManager.photoDetailCheckImage
designManager.photoDetailUnCheckImage
                
designManager.photoGalleryBackButtonImage
designManager.photoGalleryOKButtonTitle
designManager.photoGalleryCheckImage
designManager.photoGalleryUnCheckImage
```

## Author

chansim.youk, dbrckstla@naver.com

## License

CSPhotoGallery is available under the MIT license. See the LICENSE file for more info.
