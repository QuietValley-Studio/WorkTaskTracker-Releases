# 工作任務追蹤 WorkTaskTracker · 工作任务追踪 · Windows Task Tracker

[繁體中文](#繁體中文) ｜ [简体中文](#简体中文) ｜ [English](#english)

**下載 Download 下载：<https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/latest>**

Windows 桌面待辦／任務追蹤工具（免安裝、離線優先、無帳號系統）／Windows 桌面待办与任务追踪工具（免安装、离线优先、无账号系统）／A portable, offline-first Windows desktop task and to-do tracker (no installation, no account, single EXE).

---

## 繁體中文

Windows 桌面待辦／任務追蹤工具，**只提供免安裝版**：單一自包含 `WorkTaskTracker.exe`，雙擊即可使用，不需要安裝、不需要管理員權限，也不需要另外安裝 .NET Runtime。

- 目前版本：**1.6.11**（檔案版本 1.6.11.0）
- 系統需求：Windows 10 / Windows 11（x64）
- 資料：單機 `tasks.json`，沒有資料庫、沒有帳號系統、不上傳任務內容

> 這個儲存庫只放**免安裝程式與使用說明**。原始碼為私有，不在這裡公開。

### 下載

**點這裡直接下載：<https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/latest>**

（打開後在頁面底部 **Assets** 區點檔名即可下載；下面表格的檔名也是直接下載連結。）

| 檔案 | 說明 | 大小 |
| --- | --- | --- |
| [WorkTaskTracker-1.6.11-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.6.11/WorkTaskTracker-1.6.11-portable-win-x64.zip) | **唯一需要下載的檔案**。解壓後含 EXE（收款碼與使用手冊都已內嵌於程式檔）與使用手冊，共 3 個檔案 | 70,604,666 bytes |

下載 ZIP → 解壓到任意資料夾 → 雙擊 `WorkTaskTracker.exe` 即可。程式資料與程式資料夾分開，換版或搬移程式都不影響任務資料。

### 校驗碼（SHA-256）

第一組是 ZIP 壓縮檔本身的校驗碼；後兩組是解壓後資料夾內 `WorkTaskTracker.exe` 與 `使用手冊.html` 的校驗碼，可用來確認解壓結果完整。

```text
WorkTaskTracker-1.6.11-portable-win-x64.zip
FE6A98D78604E3AE5C96AA826D863934B79BEBCC4EBF703F5D4362432F7ED3BF

WorkTaskTracker.exe
65B35FFED188A8994217065CDD04A637A6DC36BAD848933BA8F5126CC1EB12BB

使用手冊.html
3F3E7BFB33774379194888F1B9247CA9B4204691989F85B5B40BDB06FCEAD011
```

PowerShell 驗證方式：

```powershell
Get-FileHash .\WorkTaskTracker.exe -Algorithm SHA256
```

### 第一次啟動

- 任務資料預設放在 `E:\WorkTaskTrackerData\<Windows使用者名稱>\tasks.json`，避免同一台電腦的不同使用者誤用同一份資料。
- 若電腦沒有 E 槽，第一次開啟會請你選擇本機資料夾，不會自行更改位置。
- 實際資料路徑記在 `%LOCALAPPDATA%\WorkTaskTracker\data-directory.txt`；要搬移資料請先結束程式，複製整個資料夾後再修改這個檔案。
- 不要把資料放在網路磁碟或正在同步的共用資料夾。

### 主要功能

- 任務清單（待辦／進行中／已完成）、優先級、進度、期限提醒
- 專案／分類自訂選項、搜尋、統計卡片
- 系統匣常駐與桌面懸浮球，Ctrl+滾輪調整介面縮放（80%～150%）
- 白天／夜間主題切換，並可依時間自動切換（預設開啟）
- 介面語言切換：繁體中文／简体中文／English
- 自動備份與還原、清理舊資料、匯出 JSON
- 友情贊助（完全自願，只掃描本機收款碼，程式不經手付款）
- 問題回報：顯示 `quiet_valley@yeah.net`，按下後才把 `mailto:` 交給系統郵件程式

### 隱私與網路行為

- 沒有 `release-config.json` 時，程式完全不會發出網路請求。
- 目前版本已設定更新來源（本儲存庫的 `version.json`）：啟動時最多每 24 小時讀取一次版本清單，只下載版本號與下載網址，不自動下載或安裝新版；匿名統計端點未設定，使用統計維持停用。
- 匿名統計若啟用，每天最多送出一次版本、作業系統、介面語言與隨機安裝 ID，不含任務名稱、備註、檔名、路徑、使用者名稱或電腦名稱。
- 友情贊助不連網：收款碼自 1.6.10 起內嵌於程式檔（資料夾放同名圖片可覆蓋），不上傳金額、收款碼或付款結果，也不送出贊助事件。
- 離線手冊雙保險：使用手冊自 1.6.11 起也內嵌於程式檔，只下載單一 EXE 也能從首頁「使用手冊」按鈕開啟完整說明（程式資料夾放新版 `使用手冊.html` 可覆蓋）。

### 使用條款

- 本程式為免費軟體，按「現狀」提供，不提供任何明示或默示擔保；請自行定期匯出備份重要資料。
- 產物沒有程式碼簽章，Windows SmartScreen 可能提示「未知發行者」；請以上方的 SHA-256 校驗碼確認檔案完整。
- 贊助完全自願，不構成交易，也不提供任何解鎖、回饋或售後義務。

### 問題與建議

來信：**quiet_valley@yeah.net**（請附上程式版本與 Windows 版本，說明操作步驟與預期結果）。

---

## 简体中文

Windows 桌面待办／任务追踪工具，**只提供免安装版**：单一自包含 `WorkTaskTracker.exe`，双击即可使用，不需要安装、不需要管理员权限，也不需要另外安装 .NET Runtime。

- 当前版本：**1.6.11**（文件版本 1.6.11.0）
- 系统要求：Windows 10 / Windows 11（x64）
- 数据：单机 `tasks.json`，没有数据库、没有账号系统、不上传任务内容

> 这个仓库只放**免安装程序与使用说明**。源码为私有，不在这里公开。

### 下载

**点这里直接下载：<https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/latest>**

（打开后在页面底部 **Assets** 区点文件名即可下载；下面表格的文件名也是直接下载链接。）

| 文件 | 说明 | 大小 |
| --- | --- | --- |
| [WorkTaskTracker-1.6.11-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.6.11/WorkTaskTracker-1.6.11-portable-win-x64.zip) | **唯一需要下载的文件**。解压后含 EXE（收款码与使用手册都已内嵌于程序文件）与使用手册，共 3 个文件 | 70,604,666 bytes |

下载 ZIP → 解压到任意文件夹 → 双击 `WorkTaskTracker.exe` 即可。程序数据与程序文件夹分开，换版本或搬移程序都不影响任务数据。

### 校验码（SHA-256）

第一组是 ZIP 压缩包本身的校验码；后两组是解压后文件夹内 `WorkTaskTracker.exe` 与 `使用手冊.html` 的校验码，可用来确认解压结果完整。

```text
WorkTaskTracker-1.6.11-portable-win-x64.zip
FE6A98D78604E3AE5C96AA826D863934B79BEBCC4EBF703F5D4362432F7ED3BF

WorkTaskTracker.exe
65B35FFED188A8994217065CDD04A637A6DC36BAD848933BA8F5126CC1EB12BB

使用手冊.html
3F3E7BFB33774379194888F1B9247CA9B4204691989F85B5B40BDB06FCEAD011
```

PowerShell 验证方式：

```powershell
Get-FileHash .\WorkTaskTracker.exe -Algorithm SHA256
```

### 第一次启动

- 任务数据默认放在 `E:\WorkTaskTrackerData\<Windows用户名>\tasks.json`，避免同一台电脑的不同用户误用同一份数据。
- 如果电脑没有 E 盘，第一次打开会请你选择本地文件夹，不会自行更改位置。
- 实际数据路径记录在 `%LOCALAPPDATA%\WorkTaskTracker\data-directory.txt`；要搬移数据请先结束程序，复制整个文件夹后再修改这个文件。
- 不要把数据放在网络磁盘或正在同步的共享文件夹。

### 主要功能

- 任务清单（待办／进行中／已完成）、优先级、进度、期限提醒
- 项目／分类自定义选项、搜索、统计卡片
- 系统托盘常驻与桌面悬浮球，Ctrl+滚轮调整界面缩放（80%～150%）
- 白天／夜间主题切换，并可按时间自动切换（默认开启）
- 界面语言切换：繁體中文／简体中文／English
- 自动备份与还原、清理旧数据、导出 JSON
- 友情赞助（完全自愿，只扫描本机收款码，程序不经手付款）
- 问题反馈：显示 `quiet_valley@yeah.net`，按下后才把 `mailto:` 交给系统邮件程序

### 隐私与网络行为

- 没有 `release-config.json` 时，程序完全不会发出网络请求。
- 当前版本已设置更新来源（本仓库的 `version.json`）：启动时最多每 24 小时读取一次版本清单，只下载版本号与下载网址，不自动下载或安装新版本；匿名统计端点未设置，使用统计保持停用。
- 匿名统计若启用，每天最多发送一次版本、操作系统、界面语言与随机安装 ID，不含任务名称、备注、文件名、路径、用户名或电脑名称。
- 友情赞助不联网：收款码自 1.6.10 起内嵌于程序文件（文件夹放同名图片可覆盖），不上传金额、收款码或付款结果，也不发送赞助事件。
- 离线手册双保险：使用手册自 1.6.11 起也内嵌于程序文件，只下载单一 EXE 也能从首页「使用手册」按钮打开完整说明（程序文件夹放新版 `使用手册.html` 可覆盖）。

### 使用条款

- 本程序为免费软件，按"现状"提供，不提供任何明示或默示担保；请自行定期导出备份重要数据。
- 产物没有代码签名，Windows SmartScreen 可能提示"未知发布者"；请以上方的 SHA-256 校验码确认文件完整。
- 赞助完全自愿，不构成交易，也不提供任何解锁、回馈或售后义务。

### 问题与建议

来信：**quiet_valley@yeah.net**（请附上程序版本与 Windows 版本，说明操作步骤与预期结果）。

---

## English

A Windows desktop task / to-do tracker, available **as a portable build only**: a single self-contained `WorkTaskTracker.exe` — just download and double-click. No installation, no admin rights, no separate .NET Runtime needed.

- Current version: **1.6.11** (file version 1.6.11.0)
- Requirements: Windows 10 / Windows 11 (x64)
- Data: local `tasks.json` only — no database, no accounts, task content never leaves your machine

> This repository hosts **the portable program and its user manual** only. The source code is private and not published here.

### Download

**Direct download: <https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/latest>**

(Open the link and pick the file under **Assets** at the bottom of the page; the file name in the table below is also a direct download link.)

| File | Description | Size |
| --- | --- | --- |
| [WorkTaskTracker-1.6.11-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.6.11/WorkTaskTracker-1.6.11-portable-win-x64.zip) | **The only file you need.** Contains the EXE (QR codes and the user manual embedded in the binary) and the user manual (3 files) | 70,604,666 bytes |

Download the ZIP → extract to any folder → double-click `WorkTaskTracker.exe`. Task data lives outside the program folder, so upgrading or moving the program never touches your tasks.

### Checksums (SHA-256)

The first hash is for the ZIP file itself; the other two are for `WorkTaskTracker.exe` and `使用手冊.html` inside the extracted folder, so you can verify the extracted files as well.

```text
WorkTaskTracker-1.6.11-portable-win-x64.zip
FE6A98D78604E3AE5C96AA826D863934B79BEBCC4EBF703F5D4362432F7ED3BF

WorkTaskTracker.exe
65B35FFED188A8994217065CDD04A637A6DC36BAD848933BA8F5126CC1EB12BB

使用手冊.html (user manual)
3F3E7BFB33774379194888F1B9247CA9B4204691989F85B5B40BDB06FCEAD011
```

Verify in PowerShell:

```powershell
Get-FileHash .\WorkTaskTracker.exe -Algorithm SHA256
```

### First launch

- Task data is stored by default in `E:\WorkTaskTrackerData\<Windows user name>\tasks.json`, so different Windows accounts on the same PC don't share data by accident.
- If the PC has no E: drive, the app asks you to pick a local folder on first launch; it never changes the location on its own.
- The actual data path is recorded in `%LOCALAPPDATA%\WorkTaskTracker\data-directory.txt`. To move data: exit the app, copy the whole folder, then update that file.
- Don't put the data folder on a network drive or a cloud-synced folder.

### Features

- Task list (pending / in progress / completed), priority, progress, deadline reminders
- Custom projects / categories, search, dashboard stat cards
- System-tray resident mode and a desktop floating ball; Ctrl+wheel to zoom the UI (80%–150%)
- Light / dark theme, plus automatic switching by time of day (on by default)
- UI languages: Traditional Chinese / Simplified Chinese / English
- Automatic backups and restore, old-data cleanup, JSON export
- Voluntary sponsorship (local QR codes only — the app never handles payments)
- Feedback: shows `quiet_valley@yeah.net` and only hands a `mailto:` link to your mail app when you click

### Privacy & network behavior

- Without a `release-config.json` file, the app makes **no network requests at all**.
- This build has an update source configured (the `version.json` in this repository): at most once every 24 hours it reads the version list — version number and download URL only. It never auto-downloads or auto-installs updates. The anonymous usage-statistics endpoint is not configured, so statistics stay disabled.
- If statistics were enabled, they would send at most one report per day (version, OS, UI language, random install ID) — never task names, notes, file names, paths, user names or computer names.
- Sponsorship is offline: QR codes are embedded in the binary (a same-named image in the program folder can override them); amounts, codes or payment results are never uploaded, and no sponsorship events are sent.
- Offline manual built in: the user guide is also embedded in the EXE since 1.6.11 — even a lone EXE download can open the full guide from the home page button (a newer `使用手冊.html` beside the EXE still wins).

### Terms of use

- This program is free software, provided "as is", with no warranty; please export backups of important data regularly.
- The binaries are not code-signed, so Windows SmartScreen may show an "unknown publisher" prompt; use the SHA-256 checksums above to verify the files.
- Sponsorship is entirely voluntary — it is not a transaction and unlocks nothing.

### Contact

Email: **quiet_valley@yeah.net** (please include the app version and Windows version, plus the steps you took and what you expected).
