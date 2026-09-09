# Launcher2-Ported
 Android 4.3's Launcher2 ported to run on modern Android

TODO:
Long pressing on the home screen (not icon) should open a context menu where you should be able to change the background, or open the launcher settings to change things such as the home screen grid size, gestures (pulling down QC panel), etc.
Home screen settings.

Building:
On Windows, download Gradle 6.5.1 (https://gradle.org/releases/), extract it to a directory of your choice then add that directory to the PATH. Install the ADB command line tools (Last version for Windows 7: https://dl.google.com/android/repository/platform-tools_r34.0.4-windows.zip) and add it to PATH. Install Android Studio or the Android Studio SDK manager. Install the SDK version 29 (For Android 10), change local.properties to point to your SDK location instead and install the build tools version 29.0.3. Other versions may work, but this setup prevents the popup warning you the app is out of date on new Android versions (thanks Google for this annoyance...), while being backwards compatible with the original Android version this app was designed for. Finally, run build.cmd inside the command prompt and watch the magic happen.

On Linux or Mac OS, install Gradle 6.5.1 and ADB with your package manager of choice, as well as the Android Studio or SDK Manager. Install the SDK version 29 (For Android 10), change local.properties to point to your SDK location instead and install the build tools version 29.0.3. Finally, compile with "./gradlew assembleDebug" and install the .apk via "adb install -r "build/outputs/apk/debug/JellyBeanLauncher2-debug.apk""