# LibreSprite Android Mobile — build via GitHub Actions

This package is intended for a Windows 7 machine that does not have a usable modern Android Studio installation. The Android build runs on GitHub Actions, not on the local PC.

## GitHub

Upload the repository contents to your GitHub repository and push to `main` or `mobile-android`. The workflow `.github/workflows/build-android-mobile.yml` can also be started manually from **Actions**.

The workflow follows the official LibreSprite Android build sequence: generate native sources with `GEN_ONLY=ON`, clone `LibreSprite/ls-android-deps` into `android/`, configure the CMake path, and run Gradle.

The resulting artifact is `LibreSprite-Android-Mobile-debug` and contains `app-all_in_one-debug.apk`.

## Important

The source remains LibreSprite GPL-2.0. This mobile adaptation changes Android input/orientation behavior while retaining the LibreSprite core.
