# Num Snap

Num Snap is an Android application that captures images using the device's camera and extracts text from the images using Google ML Kit. It provides features to identify and extract phone numbers, email addresses, and names from the captured text.

## Features

- Capture images using the device's camera.
- Extract text from images using Google ML Kit.
- Identify and extract phone numbers, email addresses, and names from the extracted text.

## Getting Started

### Prerequisites

- Android Studio 4.1 or higher
- Android device or emulator running API level 24 or higher

### Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/Joojmusic/numsnap.git
    ```

2. Open the project in Android Studio.

3. Build the project to download all dependencies.

### Running the Application

1. Connect your Android device or start an emulator.

2. Grant necessary permissions to the app (Camera permission).

3. Run the app from Android Studio.

## Usage

1. Open the Num Snap app.

2. Click on the button to capture an image using the camera.

3. The captured image will be processed, and text will be extracted using Google ML Kit.

4. The app will identify and extract phone numbers, email addresses, and names from the extracted text and display them.

## Code Overview

### MainActivity.java

The main activity that handles camera intent, image capture, and text recognition using Google ML Kit.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Google ML Kit](https://developers.google.com/ml-kit) for providing the text recognition functionality.
- [Android Jetpack](https://developer.android.com/jetpack) for providing useful libraries and tools.

## Permissions

Ensure the following permissions are added in the `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.CAMERA" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />

<application
    ...>
    <provider
        android:name="androidx.core.content.FileProvider"
        android:authorities="com.example.numsnap.fileprovider"
        android:exported="false"
        android:grantUriPermissions="true">
        <meta-data
            android:name="android.support.FILE_PROVIDER_PATHS"
            android:resource="@xml/file_paths" />
    </provider>
</application>


