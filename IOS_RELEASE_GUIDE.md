# MinaPangutana iOS Release Guide

## What you can do on Windows now

1. Test the web app with `npm install` and `npm run serve`.
2. Host the folder over HTTPS so iPhone users can install it from Safari.
3. Maintain the question-bank logic, interface, and PWA from Windows.
4. Keep `com.orelogic.minapangutana` unchanged as the permanent app identifier.

## Install the web version on iPhone

1. Open the hosted MinaPangutana URL in Safari.
2. Tap **Share**.
3. Tap **Add to Home Screen**.
4. Confirm **Add**.

The installed PWA works offline after its first successful load.

## Prepare the App Store wrapper

Do not run `npm run ios:add` until the project is on macOS because Apple's iOS build tools require Xcode.

When you have temporary Mac access or a macOS cloud build environment:

1. Install the current supported Xcode release.
2. Copy or clone this project onto the Mac.
3. Run `npm install`.
4. Run `npm run ios:add` once.
5. Run `npm run ios:sync` after every web-code update.
6. Run `npm run ios:open` to open the project in Xcode.
7. Select your Apple developer team and retain `com.orelogic.minapangutana`.
8. Add the App Store icon and required privacy information.
9. Test on a physical iPhone through Xcode or TestFlight.
10. Archive and upload through Xcode, then complete the App Store Connect listing.

## Before App Store submission

- Join the Apple Developer Program.
- Provide a public privacy-policy URL and support URL.
- Prepare App Store screenshots for the required iPhone sizes.
- Describe imported reviewer content as locally stored.
- Avoid any implication of official PRC affiliation.
- Confirm rights to every bundled question, explanation, logo, and image.
- Test offline launch, file import, export, scoring, review, and persistence.

## Important limitation

Windows can maintain the shared app, but it cannot produce or sign the final iOS App Store archive. The final native build requires Xcode on macOS, through a Mac you control or an appropriate hosted macOS build service.
