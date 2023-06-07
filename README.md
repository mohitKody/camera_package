## Features

List what your package can do. Maybe include images, gifs, or videos.

## Getting started

* Display live camera preview in a widget.
* Snapshots can be captured and saved to a file.
* Custom image quality compressor.
* Image cropper

## installation

* Camera permission in androidmanifest
* Add following crop conditions in manifest :

 ```dart
<uses-permission android:name="android.permission.CAMERA"/>

<activity
android:name="com.yalantis.ucrop.UCropActivity"
android:screenOrientation="portrait"
android:theme="@style/Theme.AppCompat.Light.NoActionBar"/>
```

## Usage

To Use the package firstly navigate to the particular class. Here which is CameraControl() and
define the image quality as per requirement from 0 to 100.

```dart
@ElevatedButton(
    onPressed: () {
      Navigator.push(
          context,
          MaterialPageRoute(
              builder: (context) =>
                  CameraControl(
                    compressQuality: 50,
                  ))).then((value) {
        setState(() {
          selected_image = File(value.path);
          //selected_image is a local variable where the image will be stored

        });
        print(selected_image!.path);
      });
    },
    child: Text("Pick Image"))
 ```

## Additional information

Tell users more about the package: where to find more information, how to
contribute to the package, how to file issues, what response they can expect
from the package authors, and more.

