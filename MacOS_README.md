# Antigravity — Clean Uninstall & Reinstall Guide

A complete guide to fully removing Antigravity and performing a fresh reinstall, including hidden files, Keychain credentials, and quota reset tips.

---

## Step 1 — Uninstall Antigravity

Delete the application:

```
/Applications/Antigravity.app
```

Drag it to Trash, or delete it directly.

---

## Step 2 — Remove Hidden Antigravity Files ⚠️ Important

Antigravity stores cache and config files (similar to VS Code) that persist after uninstall. Open **Terminal** and run:

```bash
rm -rf ~/Library/Application\ Support/Antigravity
rm -rf ~/Library/Caches/Antigravity
rm -rf ~/Library/Preferences/com.google.antigravity.plist
rm -rf ~/Library/Logs/Antigravity
```

Also remove VSCode-style folders:

```bash
rm -rf ~/.antigravity
rm -rf ~/.config/antigravity
```

---

## Step 3 — Remove Keychain Credentials

Google login tokens remain in macOS Keychain even after uninstall.

1. Open **Keychain Access**
2. Search for the following terms one at a time:
   - `antigravity`
   - `google`
   - `oauth`
3. Delete any entries related to Antigravity login

---

## Step 4 — Remove Google Account Session

Quota can sometimes be tied to the Google account session used by Antigravity.

1. Open your browser and go to: [https://myaccount.google.com/device-activity](https://myaccount.google.com/device-activity)
2. Sign out from **Antigravity** or any unrecognized devices

---

## Step 5 — Restart Your Mac

Reboot so all remaining caches are cleared.

---

## Step 6 — Reinstall Antigravity

Download a fresh copy from:

```
https://antigravity.google/
```

Log in with your Google account.

✅ After completing all steps, Antigravity will behave like a fresh install.

---

## ⚠️ Important Reality — Quota May Still Be Limited

Even after clearing all local files, **Claude Opus quota may still be restricted** because quota is often tracked **server-side** by Google/Antigravity using:

- Google account identity
- IP address
- Device fingerprint

Reinstalling alone may **not** fully reset the quota.

---

## 🔥 Pro Trick — Full Quota Reset

If quota is still not reset after reinstalling, developers typically do the following:

| Step | Action |
|------|--------|
| 1 | Create a **new Google account** |
| 2 | Use a **new Chrome profile** |
| 3 | Connect via **VPN or a different IP** |
| 4 | Perform a **clean Antigravity install** |

Following all four steps together usually results in a full quota reset.
