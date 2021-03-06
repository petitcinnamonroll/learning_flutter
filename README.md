# ml_cat_dog_2

A new Flutter project.

Trying to piece together:
- how to write a Flutter App...
- how to use the image picker package
- how to implement TensorFlowLite model into Flutter (so far haven't gotten here yet) -- how to use the tflite package

### tutorials I've tried following
(to varying degrees of success)  

https://medium.com/fabcoding/adding-an-image-picker-in-a-flutter-app-pick-images-using-camera-and-gallery-photos-7f016365d856 <br />
Run tfLite model (Coding Cafe): https://www.youtube.com/watch?v=GHpzS5NXJ-A  
Image classification: https://www.youtube.com/watch?v=JLhHxTDz7K8&t=1s  
Cat-dog tutorial: https://www.youtube.com/watch?v=-5kUv47xKy0  
Running CNN model in flutter: https://medium.com/analytics-vidhya/run-cnn-model-in-flutter-10c944cadcba  

### Errors I had

**07-07-21** <br />
metal_delegate.h not found -- updating the Podfile.lock, along with following the tflite package set up instructions fixed it:
https://pub.dev/packages/tflite

ImagePicker just won't give me an image. Also, if I click on the gallery/select an image twice, it throws an error: PlatformException(multiple_request, Cancelled by a second request, null, null)

**07-08-21** <br />
Apparently this might be a problem with M1 chip: https://github.com/flutter/flutter/issues/71943

Notably, when running flutter run --verbose, got this error at the end:
TimeoutException after 0:00:00.250000: Future not completed
Which matches what I thought would be true since ImagePicker isn't giving me an image, and the print statement I had after the await isn't printing.

**07-09-21** <br />
Interestingly, when I try to get an image and then click cancel, then the after await statement prints, so it seems to just be an issue with ImagePicker.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

### Other Resources/Sources Consulted
https://stackoverflow.com/questions/64718180/saving-imagepicker-image-from-gallery-in-flutter
https://androidride.com/image-picker-flutter-take-picture/
https://dart.dev/codelabs/dart-cheatsheet
https://www.youtube.com/watch?v=7iZAZ0CwFKI - Image Picker with Flutter
https://stackoverflow.com/questions/59558604/why-do-we-use-dispose-method-in-dart-code - dispose()
https://stackoverflow.com/questions/62368886/how-to-convert-image-to-file-in-flutter - convert Image to File

### Future packages
https://github.com/fluttercandies/flutter_wechat_assets_picker

