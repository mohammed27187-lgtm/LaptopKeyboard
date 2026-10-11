# Laptop Keyboard for Android

A full-width, laptop-style soft keyboard designed for writers and spreadsheet users.

## Features

- Permanent number row (1–0)
- Full QWERTY layout
- Dedicated arrow keys and Home/End
- Ctrl modifier with Select All, Copy, Paste, Cut, and best-effort Undo shortcuts
- Shift and Caps Lock
- Symbols layer with spreadsheet-friendly characters such as `$`, `%`, `=`, `+`, brackets, and braces
- Dark theme
- Android 7.0 (API 24) and newer

## Build an installable APK

This project is source code. The APK must be built before it can be installed.

### Option A: Build with Android Studio

1. Install Android Studio and its Android SDK (API 34).
2. Open the `LaptopKeyboard` folder in Android Studio.
3. Allow Gradle to sync. Use JDK 17 and Gradle 8.2.
4. Select **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
5. Android Studio will show a notification with a link to the generated debug APK. The output path is `app/build/outputs/apk/debug/app-debug.apk`.

### Option B: Build using GitHub Actions

A workflow is included at `.github/workflows/android.yml`.

1. Upload this project to a GitHub repository.
2. Open the repository's **Actions** tab and run **Build Android APK**, or push a commit.
3. When the workflow succeeds, open the run and download the `LaptopKeyboard-debug-apk` artifact.
4. Extract the artifact to get `app-debug.apk`, then transfer it to your Android phone and install it. Android may ask you to allow installs from that source.

## Enable the keyboard on your phone

1. Install and open **Laptop Keyboard**.
2. Tap **Enable Laptop Keyboard** and enable it in Android's input-method settings.
3. Tap **Select Laptop Keyboard** and choose **Laptop Keyboard**.
4. Open a text field and select the keyboard from the input-method picker if needed.

You can switch back to another keyboard at any time through Android's keyboard settings.

## Important notes

- This is a debug build setup, not a signed Play Store release.
- Ctrl shortcuts depend on the app being typed into. Some apps do not support context-menu actions or Undo in the same way.
- The classic Android `Keyboard` / `KeyboardView` API used by this project is deprecated. It may still run, but behavior should be tested on the target phone and in apps such as Excel before relying on it.
