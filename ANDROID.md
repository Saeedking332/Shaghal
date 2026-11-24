# Shaghal on Android

The repository keeps the Flutter sources in `lib/` and generates the native app project when needed.

## Build locally

Requirements: Flutter stable, Android SDK, and Java 17.

```bash
chmod +x setup_android.sh
./setup_android.sh
cd app
flutter run
```

To build a release APK:

```bash
flutter build apk --release
```

The APK is written to `app/build/app/outputs/flutter-apk/app-release.apk`.

## GitHub Actions

The **Build Android APK** workflow runs on pushes to `main` and `android-preview`, and can also be started manually from the Actions tab. Successful builds are uploaded as the `Shaghal-android-apk` workflow artifact.

Android media playback uses `media_kit_libs_android_video`. Background playback and lock-screen controls are registered through `audio_service`.
