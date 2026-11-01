# HOLO.01 — Android prototype

This repository builds a debug APK through GitHub Actions. It is a prototype, not a finished hands-free gesture-control system.

## Included now
- Native Android launch screen.
- Permission flow for displaying a floating overlay above other apps.
- Foreground service that displays a movable HOLO.01 interface.
- Touch controls for rotating the centre element, hiding panels, and resetting the scene.
- An Accessibility Service declaration reserved for later explicit gesture commands.

## Not implemented yet
- Camera-based hand tracking.
- Gesture recognition.
- Mapping hand movements to Android actions.
- General hands-free control of other apps.
- A physical hologram; the current interface is rendered on the phone display.

## Build the APK with GitHub (phone-friendly)
1. Create a new **empty** GitHub repository named `HOLO-01`. Do not add a README, licence, or `.gitignore` on GitHub.
2. Extract this ZIP on your phone.
3. Open the extracted `HOLO-01-CORRECTED` folder. Upload the **contents inside it** to the repository root, not the folder itself. Include the hidden `.github/workflows/android-apk.yml` file.
4. Commit the files to the `main` branch.
5. Open the repository's **Actions** tab. Select **Build HOLO.01 APK**. If it did not start automatically, choose **Run workflow**.
6. Wait for the run to finish. Open the successful run and download the `HOLO-01-debug-apk` artifact.
7. Extract the downloaded artifact ZIP. It contains `app-debug.apk`. Install that APK on your Android phone.

## First device test
1. Open HOLO.01.
2. Tap **DEPLOY HOLO.01**.
3. Grant Android's **Display over other apps** permission.
4. Return to HOLO.01 and tap **DEPLOY HOLO.01** again.
5. Confirm the floating interface appears. Tap the × to close it.

The **ENABLE PHONE CONTROL** button opens Android Accessibility settings, but this prototype does not yet use camera hand tracking or send hand-gesture commands. Do not enable Accessibility for this prototype unless you are deliberately testing that permission.

## Technical details
- Package/application ID: `com.visphos.holo01`
- Minimum Android version: Android 8.0 (API 26)
- Compile SDK: 35
- JDK: 17
- Android Gradle Plugin: 8.7.3
- Gradle: 8.9
