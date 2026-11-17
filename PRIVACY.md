# Privacy Policy — paipu-hub (v1.0.0)

**Last Updated:** 2026-11-17

**paipu-hub** is a local-first Riichi Mahjong replay collector, statistics dashboard, and 3D AI review extension for Google Chrome. Your privacy is fundamental to how the extension is built: **paipu-hub operates 100% locally in your browser and has no developer-operated backend servers, user accounts, analytics, or tracking.**

---

## 1. Data Accessed and Handled Locally

To perform its single purpose of collecting, deduplicating, and analyzing your Mahjong replays, the extension accesses and processes the following data **strictly on your local device**:

1. **Website Content (Mahjong Replays & AI Reviews)**
   - When you click **"Add to Library"** (or enable the optional **Auto** capture toggle) on supported replay/AI review sites, or manually paste a replay URL / `tenhou6` JSON into the dashboard, the extension reads the game log, round events, scores, and AI evaluation weights from that page.
   - On **Mahjong Soul** domains (`game.maj-soul.com`, `game.maj-soul.net`, `game.mahjongsoul.com`, `mahjongsoul.game.yo-star.com`), a passive `MAIN`-world observer (`content/majsoul-hook.js`) inspects binary WebSocket replay messages inside your active tab solely to reconstruct the replay record locally when you open a match log. It does not automate gameplay, modify requests, or transmit data to any external server.
2. **Web History (Supported Replay URLs Only)**
   - The extension inspects the URL of your active tab **only** when it matches the supported Mahjong replay/AI domains declared in `manifest.json` (`tenhou.net`, `mjai.ekyu.moe`, `gokujan.com`, `naga.dmv.nico`, `rc.honk.li`, `riichi.miai.moe`, and the Mahjong Soul domains above). This is used solely to show the capture card and prevent duplicate imports. Browsing history outside those domains is never accessed or recorded.
3. **Personally Identifiable Information (Player Nicknames & Mahjong Soul Account ID)**
   - Replay logs contain the table players' display nicknames. On Mahjong Soul, the extension also reads the signed-in `account_id` from the open game page solely to automatically identify which seat (East/South/West/North) corresponds to your point of view. Neither nicknames nor account IDs leave your browser.

---

## 2. Where Data Is Stored & Network Requests

- **100% Local Storage:** All captured games, computed statistics, bookmarks, spaced-repetition drill progress, and UI preferences (language/theme) are stored exclusively inside your browser's local **IndexedDB** and **`chrome.storage`**.
- **Zero Developer Servers:** The developer does not collect, receive, store, or have access to any of your replays, account IDs, or browsing data.
- **Direct Platform Requests Only:** When you trigger a fetch or import by URL, your browser communicates directly with the corresponding supported Mahjong/AI website listed in `host_permissions`. No proxy or third-party analytics endpoint is involved.
- **Optional Local Folder Auto-Backup:** If you explicitly enable the File System Access auto-backup feature, compressed `.json.gz` backups are written only to the local folder you selected on your device.

---

## 3. Chrome Web Store Limited Use & Third-Party Sharing

In compliance with the **Chrome Web Store User Data Policy** (including the Limited Use requirements):
- **No Sale or Transfer:** paipu-hub does **not** sell, rent, or transfer user data to third parties.
- **No Advertising or Profiling:** User data is never used for personalized advertising, marketing, or creditworthiness/lending determination.
- **No Remote Code:** All scripts, stylesheets, and 3D assets (including Three.js) are bundled directly inside the extension package.

---

## 4. Your Control & Data Deletion

- **Export:** You can export your full local database at any time as `.json` or `.json.gz` from the dashboard.
- **Delete:** You can delete individual games, click **"Clear"** in the dashboard to wipe IndexedDB, or uninstall the extension to remove all locally stored extension data permanently.

---

## 5. Contact

- **Developer:** Kenneth Chan
- **X (Twitter):** [@kennethkkchan](https://x.com/kennethkkchan)

---

# 隱私權政策 — paipu-hub (v1.0.0)（繁體中文摘要）

**最後更新日期：** 2026-11-17

**paipu-hub** 是一款純本機運行的日本麻將牌譜收集管理台與 3D AI 複盤工具。**本擴充功能沒有任何開發者伺服器、不需要註冊帳號，也不含任何遙測、廣告或追蹤程式碼。**

1. **僅於本機處理的資料範圍**：
   - **網頁內容**：當你在支援的牌譜或 AI 分析網站點擊「加入牌譜庫」（或啟用自動收錄）時，擴充功能會讀取該場牌譜對局事件、分數與 AI 權重；在雀魂網域上，被動式 WebSocket 觀察腳本（`majsoul-hook.js`）僅於你打開牌譜時在瀏覽器內還原該場牌譜，不進行任何自動操作或外部傳輸。
   - **網頁紀錄（僅限支援網域）**：僅檢查符合 `manifest.json` 所列麻將網域的目前分頁網址，用於辨識平台與去重，不會存取其他任何網站的瀏覽紀錄。
   - **個人識別資訊（玩家暱稱與雀魂 `account_id`）**：僅用於在本機自動辨識哪一家是你本人視角，絕不離開你的瀏覽器。
2. **純本機儲存**：所有牌譜、統計數據、盲測練習進度與語言／主題設定皆只儲存在你自己的瀏覽器 `IndexedDB` 與 `chrome.storage` 中；開發者無法存取你的任何資料。
3. **不販售、不分享、不轉傳第三方**：完全遵守 Google Chrome Web Store 使用者資料政策與有限使用（Limited Use）規範。
4. **資料控制權**：你可隨時在管理台匯出 `.json` / `.json.gz` 備份、清空資料庫，或移除擴充功能以徹底刪除本機資料。
