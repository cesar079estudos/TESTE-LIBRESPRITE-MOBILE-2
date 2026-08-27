# LibreSprite Android Mobile — Windows 7 build route

The Windows 7 machine is intentionally **not** used to compile the Android native code.
Current Android Studio requires 64-bit Windows 10 or newer, and the current LibreSprite Android
workflow is already designed to build on a Linux CI runner. This project therefore uses GitHub
Actions for the actual Android build.

## Result

The workflow produces a debug APK artifact named:

`LibreSprite-Android-Mobile-debug`

The APK is the `all_in_one` debug variant.

## Why this route

LibreSprite's official installation instructions say the Android build uses the separate
`ls-android-deps` repository. The official Android repository contains the Gradle wrapper and
Android-specific native dependencies. The workflow fetches that repository on the runner, so the
Windows 7 machine does not need Android Studio, SDK, NDK, or CMake for the Android build.

## Local source

The source tree remains buildable as the normal LibreSprite project. Android-specific behavior is
kept behind `__ANDROID__` in the SDL2 system layer.
