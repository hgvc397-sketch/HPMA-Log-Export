[繁體中文](./README.md) | **English**

# HPMA Data Exporter (Beginner's Guide)

Back up your *Harry Potter: Magic Awakened* Android account data, battle decks, wardrobe outfits, chat history, personal artwork, and **3D character & Fantastic Beast models** locally on your device.

> **Supported Editions**: TW/HK/MO, CN (Official & Channels), Global / International, Japan (JP), and Korea (KR)  
> **Requirements**: Android 8.0 or newer (works on regular non-root phones, rooted phones, and Android emulators such as MuMu Player; built-in Traditional Chinese / English toggle)

---

## ⚠ Important Notice (Read First for Non-Root Phones)

The TW/HK/MO and JP servers have announced **top-up suspension on December 21, 2026, and official server shutdown on March 3, 2027**.

- **Regular (Non-Root) Phones**: Text data, decks, and personal media can be backed up via Shizuku. **3D Character Preview** and **Save Character Model ZIP** fetch model files on demand from the official CDN by default—**please complete your 3D extraction and save the ZIP to your PC or cloud storage well before official server shutdown**.
- **Rooted Phones / Android Emulators**: Enable **Root Deep Mode** on the home screen to read the stock game's model archives directly offline without Shizuku. As long as the stock game data remains on your device, you can continue extracting even after server shutdown.

---

## 1. Download APK

Go to **[Releases](../../releases)** on the right side of this page to download the latest APK:

- **`HPMA-TW-Log-Export-1.6.18-noImport.apk`**
  - Includes everything: full account backup JSON, redacted shareable JSON, media & files ZIP, character & deck preview, 3D Character Preview (including all 98 original sculpted preset faces), Save Character Model ZIP, and Fantastic Beast 3D Preview.

---

## 2. Before You Start: Open Key Screens in the Stock Game

The game only writes **recently viewed content** into your phone's local cache and logs. Before backing up, open the stock game and spend ~3 minutes visiting the following screens:

1. **Decks & Battle Data**: Enter one practice match or duel with each deck you want to save (records echo affixes, card levels, proficiency, Patronus, brooms, and card skins).
2. **Wardrobe & Outfits**: Switch into several outfits you want archived, and open the **Wands, Titles, Avatar Frames, Echoes, and Wizard Space Furniture** tabs.
3. **Dormitory & Chat**: Open the **Dormitory Guestbook** and **Chat** once (updates check-in days, messages, profile photos, and duel ranks).
4. **Wizard Space**: Visit your own space once so the game generates the latest thumbnail records.

---

## 3. Complete Your Backup in 5 Steps

### Step 1: Install the App
1. Download the APK to your phone from **[Releases](../../releases)**.
2. Tap the APK file to install. If prompted that installing unknown apps is not allowed, follow the on-screen prompt to enable "Allow from this source".

### Step 2: Set Up Read Access (Choose One)

- **A. Regular Phones (Non-Root) — Using Shizuku**
  1. Open this app. If you are new to Shizuku, tap **Setup Guide & FAQ** at the bottom of the home screen (includes a built-in setup animation and brand-specific background-keeping tips).
  2. You can also follow the [Official Shizuku Setup Guide](https://shizuku.rikka.app/guide/setup/) to pair and start Shizuku using built-in **Wireless debugging** (no PC required on Android 11+).
- **B. Rooted Phones / Emulators (e.g., MuMu Player)**
  - No Shizuku needed! Simply check **Root Deep Mode** on the home screen and tap Allow when the superuser prompt appears.

### Step 3: Select Game Edition & Capture Data
1. Under **1. Source & Capture**, select your game edition (defaults to TW/HK/MO; tap `EN` / `繁中` in the top-right corner to switch languages).
2. Tap **Grant Access** (to authorize Shizuku) or **Auto Capture**.
3. Wait a few seconds for local parsing. The screen will show the number of logs, characters, outfits, decks, and cache entries read.
   > After viewing more outfits or decks in the stock game, come back and tap **Auto Capture** again—the app **automatically merges and preserves previous records** without overwriting older decks or outfits.

### Step 4: Preview & Save Backup Files
Under **2. Preview & Backup**:
1. Tap **Preview Character, Decks & Collection** to verify that your character info, duel ranks, decks, and collections were captured.
2. Save the files you need (all categories are selected by default, or you can pick specific ones):
   - **Save JSON**: **Full personal backup** (contains personal identifiers, chat logs, and photo URLs—keep it private and **do not upload it publicly**).
   - **Save Redacted JSON (Shareable)**: Automatically masks account IDs, UIDs, chat contents, and private URLs, making it safe to share with friends or communities.
   - **Save Media & Files ZIP**: Packs Wizard Space thumbnails, DIY flowers/plates/hats/cakes, profile photos, and custom uploaded emojis.

### Step 5: Preview & Save 3D Character Models
Under **3. 3D Character & Beast Models**:
1. Tap **3D Character Preview**: Drag to rotate, pinch to zoom, and switch between **Face** and **Full body** to inspect your current outfit, face, and makeup (supports all 190 face presets including all 98 original sculpted faces, hair dyeing, outfit dyeing, and hat-hair rules).
2. Tap **Save Character Model ZIP**: Packs the raw 3D model files (`.mesh`, `.mb` blendshapes, `.astc` textures, and `face_recipe.json`) into a single ZIP for long-term preservation, which can later be converted on a PC to standard 3D formats (OBJ + PNG).
3. Tap **Fantastic Beast 3D Preview**: View the default 3D models of 22 Fantastic Beasts (Niffler, Mooncalf, Lapifors, etc.).

---

## 4. FAQ

### Q1: Is this tool safe? Does it upload my account data?
- **No**. Log parsing, cache decryption, and backup packing are all performed **locally on your phone**. No personal account data is ever uploaded to any third-party server.
- The only network request occurs on non-root phones when using **3D Character Preview / Save Character Model ZIP**, which downloads public 3D model and texture files from the official game CDN (no personal data is sent).

### Q2: Why does "Auto Capture" fail after I reboot my phone?
- Android stops Shizuku upon reboot. Open Shizuku to start the service again, then return to this app and tap **Auto Capture**.

### Q3: What if "3D Character Preview" fails or gets stuck?
- On non-root phones, make sure you have an active internet connection (Wi-Fi recommended). The first preview downloads the model parts used by your character; subsequent previews load instantly from the local cache.
- On rooted phones or emulators, check **Root Deep Mode** on the home screen to read directly from local game folders.

### Q4: Can I use this on Android 11+ without Shizuku?
- Yes, via **Import Logs Manually** at the bottom of the home screen. Use a PC over USB to copy `log.txt` and `log_old_*.txt` from the game folder into your phone's Download folder, then select them in the app. Note that manual mode only imports text logs and cannot pack `Documents/` personal media.

### Q5: What cannot be saved by this exporter?
- Items that only exist on the official server and have never been opened on your phone, as well as real-time Gem / Gold balances, do not appear in local caches. We recommend taking **in-game screenshots or screen recordings** alongside your backup.

---

> This tool is completely free for players to back up their personal memories. Do not buy or fall for paid resellers.
