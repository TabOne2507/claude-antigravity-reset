# 🧹 Completely Remove Antigravity from Windows

A step-by-step guide to fully uninstall Antigravity, clear all cached data, and optionally reinstall with a fresh quota.

---

## 1️⃣ Uninstall Antigravity

Navigate to:

```
Settings → Apps → Installed Apps
```

Search for **Google Antigravity** and click **Uninstall**.

---

## 2️⃣ Delete Local App Data ⚠️ IMPORTANT

Open **Run** (`Win + R`) and delete the following folders:

**Folder 1:**
```
%APPDATA%\Antigravity
```

**Folder 2:**
```
%LOCALAPPDATA%\Antigravity
```

These folders contain:
- Login sessions
- Cached model tokens
- Workspace data
- Logs and temporary files

Delete them completely.

---

## 3️⃣ Delete Installation Folder

If still present, delete one of the following:

```
C:\Program Files\Google\Antigravity
```

or

```
C:\Program Files\Antigravity
```

> The default installation path is usually inside `Program Files`.

---

## 4️⃣ Remove Hidden Config

Open **File Explorer** and delete these if they exist:

```
C:\Users\<your-username>\.antigravity
C:\Users\<your-username>\.config\antigravity
```

---

## 5️⃣ Clear Browser Login Session

Antigravity login uses **Google OAuth** via browser. To clear the session:

1. Open **Chrome**
2. Navigate to:
   ```
   chrome://settings/siteData
   ```
3. Search for and remove:
   ```
   antigravity
   google oauth
   ```

> Alternatively, use a **new Chrome profile** to ensure a completely clean session.

---

## 6️⃣ Restart Windows

Reboot your PC to clear any remaining cached sessions from memory.

---

## 7️⃣ Reinstall Antigravity

Download and reinstall Antigravity, preferably to:

```
C:\Program Files\Google\Antigravity
```

Then log in with your Google account.

---

## ⚠️ Why Quota May Still Not Reset

Even after a full cleanup, quota can be tracked by:

- **Google account**
- **Device fingerprint**
- **IP address**

To fully reset quota, many developers use a combination of:

| Method | Description |
|--------|-------------|
| 1️⃣ New Google account | Creates a fresh identity |
| 2️⃣ New Chrome profile | Isolates browser session |
| 3️⃣ Different IP | Use a VPN or mobile hotspot |
| 4️⃣ Fresh Antigravity install | Clears all local state |

---

## 💡 Pro Tip — Multiple Instances for Developers

Instead of reinstalling every time, run multiple Antigravity instances in **Windows Sandbox** or a **VM** so each environment gets a fresh quota without affecting your main setup.

---
