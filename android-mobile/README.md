# LibreSprite Android Mobile port

This branch is intended to turn LibreSprite into a portrait-first Android build while preserving
the existing C++ editor core.

Current mobile foundation:

- Android portrait orientation hint.
- SDL touch-to-mouse translation enabled on Android so existing editor tools continue to receive
  pointer input.
- Existing LibreSprite touch magnification path is preserved.
- GitHub Actions build route that uses the official `ls-android-deps` repository.

The Android dependency tree is deliberately not vendored into this source archive because it is a
separate official LibreSprite repository and is fetched by the build workflow.
