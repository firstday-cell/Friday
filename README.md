# JARVIS AI — Android starter project

A beginner-friendly, free Kotlin + Jetpack Compose starter for an Iron Man-inspired personal assistant UI.

## Included
- Futuristic cyan-on-dark HUD interface
- Android speech input using the system speech-recognition activity
- Spoken replies using Android TextToSpeech
- Commands to open Google, YouTube, ChatGPT, WhatsApp, Chrome, Camera, Settings, and Clock/Alarms
- Local note memory using SharedPreferences
- Timed reminders with Android notifications (for example: `remind me to study in 10 minutes`)
- Activity log and command help

## Important limitations
- This starter does **not** contain an embedded AI language model. The **OPEN AI CHAT** button opens ChatGPT in a browser. To add in-app AI conversation, connect an AI API through a secure backend; do not ship a private API key in the Android app.
- Voice recognition depends on a compatible speech service and may require internet.
- Reminder timing is inexact on modern Android and notifications require permission. Battery restrictions may delay notifications. This starter does not restore scheduled reminders after a device reboot.
- It does not continuously listen for a wake word in the background.

## Build on Android or a computer
1. Install Android Studio on a computer from https://developer.android.com/studio.
2. Extract `JarvisAI.zip`.
3. In Android Studio, choose **Open** and select the extracted `JarvisAI` folder.
4. Let Gradle sync. Use JDK 17 and install Android SDK 35 if Android Studio asks.
5. Connect your Android phone with USB debugging enabled, or use an emulator.
6. Press **Run**. If Android asks for notification permission, allow it to test reminders.
7. To make an APK, choose **Build → Build Bundle(s) / APK(s) → Build APK(s)**. Android Studio will show the output location.

## Example commands
- `hello`
- `what time is it`
- `open YouTube`
- `open Google`
- `open WhatsApp`
- `open camera`
- `open settings`
- `remember that my exam is Monday`
- `show memory`
- `clear memory`
- `remind me to study in 10 minutes`
- `remind me to call home in 2 hours`
- `help`

## Troubleshooting
- If voice input doesn't open, test typing a command and check whether a speech recognition service is installed/enabled on the phone.
- If app launching fails, Android may not have that app installed; web links open in the browser.
- If notifications do not arrive, allow notifications for JARVIS AI and check battery restrictions.

## Build the APK for free using GitHub Actions (phone-friendly)
1. Create a GitHub account and a new repository named `JarvisAI`.
2. Upload the **contents** of this project folder to the repository (including the hidden `.github` folder). You can do this from GitHub's website, or upload the ZIP contents from a computer.
3. Open the repository's **Actions** tab and choose **Build JARVIS APK**. If prompted, enable Actions, then press **Run workflow**.
4. Wait for the workflow to finish successfully. Open that run and download the `JarvisAI-debug-apk` artifact.
5. Extract the downloaded artifact ZIP to get `app-debug.apk`, then open it on your Android phone and approve installation from that source if Android asks.

This produces a debug APK for personal testing, not a Play Store release. The APK is not prebuilt in this source ZIP; GitHub Actions builds it when you run the workflow.
