# Sortshot

Sortshot files the photos you take with your phone's own camera into the folder you choose.
On a Samsung phone every photo lands in one Camera folder; with Sortshot you pick a folder, tap Shoot,
and what you take is in that folder when the camera closes. It has no adverts, no accounts and no paid version.

- Website: https://customgpter.github.io/sortshot/
- Latest app file: https://github.com/CustomGPTer/sortshot/releases/latest
- Privacy: https://customgpter.github.io/sortshot/privacy.html

## What it does

- Opens the phone's full camera and moves what you take into the chosen folder when it closes
- Folders and sub-folders in DCIM/Sortshot, home-screen shortcuts, a quick-settings tile
- Tags and notes (typed or dictated), written into JPEG files so they travel with the photo
- Optional date and time, and latitude and longitude, printed on each photo as it is filed
- Search across folders, a review screen for each session, stamped copies, PDF report, zip export
- Google Drive backup of chosen folders to your own Drive, using only the "files this app created" permission
- Hide folders from the Gallery, and a 30-day bin

## Building

The app is in the `android` folder. It needs JDK 17 or newer and the Android SDK (platform 36).

    cd android
    ./gradlew testReleaseUnitTest assembleDebug

A release build needs your own signing key: make a `keys` folder beside `android/build.gradle.kts` holding
your keystore and a `signing.properties` file with `storeFile`, `storePassword`, `keyAlias` and `keyPassword`.
Google Drive sign-in works only in a copy signed with a key registered for the app with Google.

## Licence

© 2026 Jonathan Jackson. Published under the GNU General Public License, version 3 (see `LICENSE`).

As an additional permission under section 7 of that licence, you may combine Sortshot with Google Play
services and distribute the result, provided you follow the licence for everything else.
