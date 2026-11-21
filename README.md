<p align="center"><img src="chrome/images/loading.png" width="32" alt="Classic green spinner"></p>

<h1 align="center">GreenSpin-Firefox</h1>

<p align="center">Brings back the classic grey and green tab loading spinners from Firefox 4–29.</p>

<p align="center">
  <img src="https://img.shields.io/badge/Firefox-userChrome.css-FF7139?style=flat-square&logo=firefoxbrowser&logoColor=white" alt="Firefox userChrome.css">
  <img src="https://img.shields.io/badge/platform-macOS%20%7C%20Windows%20%7C%20Linux-lightgrey?style=flat-square" alt="Platforms">
  <img src="https://img.shields.io/badge/CSS-663399?style=flat-square&logo=css&logoColor=white" alt="CSS">
</p>

A small `userChrome.css` patch that replaces the modern tab throbber with the old Firefox spinners. It touches nothing else in the UI.

## What it does

| State | Spinner |
|---|---|
| Connecting (DNS / TCP) | <img src="chrome/images/connecting.png" width="16" alt=""> Grey circle |
| Loading page content | <img src="chrome/images/loading.png" width="16" alt=""> Green spinning circle |

- Hides the default SVG throbber and swaps in the original animated PNGs
- Brightens both spinners in dark mode so they stay visible
- Two images, one stylesheet, one pref

## Install

1. Open your profile folder: `about:support` → **Profile Folder** → **Open Folder**.
2. Copy the `chrome` folder into it.
3. Enable custom stylesheets: either copy `user.js` into the profile folder, or set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true` in `about:config`. If you already have a `user.js`, append this line instead of replacing it:

   ```js
   user_pref("toolkit.legacyUserProfileCustomizations.stylesheets", true);
   ```

4. Restart Firefox.

Profile folder locations:

- macOS: `~/Library/Application Support/Firefox/Profiles/<profile>/`
- Windows: `%APPDATA%\Mozilla\Firefox\Profiles\<profile>\`
- Linux: `~/.mozilla/firefox/<profile>/`

## Uninstall

Delete `chrome/` (and the `user.js` line, if you added it) from the profile folder and restart Firefox.

## Compatibility

Works on Firefox Release and ESR on macOS and Windows. Linux should work but is untested.
