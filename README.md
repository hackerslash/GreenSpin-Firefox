# Classic Firefox Green Spinner

A minimal Firefox theme that replaces the modern tab loading spinner with the classic **grey connecting circle** and **green spinning loader** from old Firefox (Firefox 4–29 era).

This theme does **one thing only** — it patches the tab throbber. No other UI changes are made, making it fully compatible with all platforms including macOS.

---

## What it does

| State | Spinner |
|-------|---------|
| Connecting to server (DNS / TCP) | Grey circle |
| Downloading page content | Classic green spinning circle |

In **dark mode**, both spinners are automatically brightened so they remain visible.

---

## Manual Installation

### Step 1 — Enable userChrome.css in Firefox

Open Firefox and navigate to `about:config`. Search for:

```
toolkit.legacyUserProfileCustomizations.stylesheets
```

Set it to **`true`**. (The `user.js` file in this folder does this automatically if you copy it across.)

---

### Step 2 — Find your Firefox Profile Folder

Open `about:support` in Firefox. Under **Application Basics**, find **Profile Folder** and click **Open Folder**.

---

### Step 3 — Copy Theme Files

Copy the `chrome` folder and `user.js` from this directory into your Firefox profile folder.

#### macOS

```bash
cp -R "/path/to/Classic-Loader-Theme/chrome" ~/Library/Application\ Support/Firefox/Profiles/<your-profile>/
cp "/path/to/Classic-Loader-Theme/user.js" ~/Library/Application\ Support/Firefox/Profiles/<your-profile>/
```

Or just drag and drop the `chrome` folder and `user.js` into the profile folder opened in Step 2.

#### Windows

Copy the `chrome` folder and `user.js` into your profile folder. The profile folder is usually located at:

```
C:\Users\<YourName>\AppData\Roaming\Mozilla\Firefox\Profiles\<your-profile>\
```

You can also press `Win + R` and type `%APPDATA%\Mozilla\Firefox\Profiles\` to open it directly.

---

### Step 4 — Restart Firefox

Completely close Firefox and reopen it. The classic green spinner will now appear when loading tabs.

---

## AI-Assisted Installation

You can ask an AI coding agent (such as [Antigravity](https://antigravity.dev)) to install this theme for you automatically.

### How to do it

1. Open your AI agent terminal/CLI **inside this folder** (or tell it the path to this folder).
2. Say: **"Install this theme into my Firefox profile"**

The agent will automatically detect your Firefox profile, copy the files, and configure `user.js`.

---

> [!WARNING]
> ### macOS — Terminal Accessibility Permission Required
>
> On macOS, the AI agent runs inside your Terminal. For the agent to be able to copy files into system-protected locations (like the Firefox application bundle or certain Library paths), **Terminal must have Full Disk Access**.
>
> To grant this:
> 1. Open **System Settings** → **Privacy & Security** → **Full Disk Access**
> 2. Enable the toggle next to **Terminal** (or whichever terminal app you use, e.g. iTerm2)
> 3. Restart your terminal and run the agent again
>
> Without this, the agent will encounter `Operation not permitted` errors even with `sudo`.

---

## Uninstall

Delete the `chrome` folder and `user.js` from your Firefox profile folder, then restart Firefox. Everything returns to normal.

```bash
# macOS
rm -rf ~/Library/Application\ Support/Firefox/Profiles/<your-profile>/chrome
rm ~/Library/Application\ Support/Firefox/Profiles/<your-profile>/user.js
```

```
# Windows — delete these from your profile folder:
chrome\
user.js
```

---

## Compatibility

| Platform | Status |
|----------|--------|
| macOS | ✅ Fully working |
| Windows | ✅ Fully working |
| Linux | ✅ Should work |
| Firefox ESR | ✅ Recommended |
| Firefox Release | ✅ Works |
