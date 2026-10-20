# Habit OS Android APK project

This project wraps the original `index.html` inside a local Android WebView. The HTML, CSS and JavaScript are copied unchanged into `app/src/main/assets/index.html`, so the app's existing design, icons (emoji/text), charts and localStorage logic remain part of the APK.

## Build an APK using only your phone + GitHub
1. Upload the contents of this project to a new GitHub repository (the `app`, `.github`, and Gradle files must be at the repository root).
2. Open the repository's **Actions** tab and enable Actions if asked.
3. Select **Build Habit OS APK** → **Run workflow**.
4. When the run finishes, open it and scroll to **Artifacts**.
5. Download `Habit-OS-APK`, extract the ZIP, then install `app-debug.apk` on your Android phone. Allow installation from your browser/file manager if Android asks.

## Size and offline behavior
- This app bundles a small HTML file and uses Android's built-in WebView. It should be comfortably below 100 MB; check the actual APK artifact after building.
- The app loads its HTML locally and does not need internet to run. Internet is only needed for the GitHub cloud build and downloading the APK.
- Habit data is stored locally by WebView on the device. This project does not add cloud backup or notifications.
- The APK uses a basic mint check-mark launcher icon. Existing in-app UI is not redesigned.
