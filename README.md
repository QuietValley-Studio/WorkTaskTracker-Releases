# 工作任務追蹤 WorkTaskTracker · 工作任务追踪 · Windows Task Tracker

[繁體中文](#繁體中文) ｜ [简体中文](#简体中文) ｜ [English](#english)

**下載 Download 下载：<https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/latest>**

Windows 桌面任務／待辦追蹤工具（免安裝、離線優先、無帳號系統）／Windows 桌面任务与待办追踪工具（免安装、离线优先、无账号系统）／A portable, offline-first Windows desktop task and to-do tracker (no installation, no account, single EXE).

---

## 繁體中文

Windows 桌面任務／待辦追蹤工具，**只提供免安裝版**：單一自包含 `WorkTaskTracker.exe`，雙擊即可使用，不需要安裝、不需要管理員權限，也不需要另外安裝 .NET Runtime。

- 目前版本：**1.0.0**（首個公開版本，檔案版本 1.0.0.0）
- 系統需求：Windows 10 / Windows 11（x64）
- 資料：單機 `tasks.json`，沒有資料庫、沒有帳號系統、不上傳任務內容

> 這個儲存庫只放**免安裝程式與使用說明**。原始碼為私有，不在這裡公開。

### 下載

| 檔案 | 說明 | 大小 |
| --- | --- | --- |
| [WorkTaskTracker-1.0.0-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.0.0/WorkTaskTracker-1.0.0-portable-win-x64.zip) | **唯一需要下載的檔案**。解壓後只有 EXE（收款碼、使用手冊與發佈設定都已內嵌）與使用手冊，共 2 個檔案 | 70,935,072 bytes |

下載 ZIP → 解壓到任意資料夾 → 雙擊 `WorkTaskTracker.exe`。任務資料與程式資料夾分開，換版或搬移程式都不影響任務資料。

### 校驗碼（SHA-256）

```text
WorkTaskTracker-1.0.0-portable-win-x64.zip
4E06CEC57C1FA41A207DB9B0B420AC9FCA55115AB727E425C47D69B337685662

WorkTaskTracker.exe
2F3C2F2DB72FAB13855A85B85205331AB987951498A89E968D0FF532A832FC22

使用手冊.html
E89BBC24DEFE5B8B381BA13CE96A2413F869239479A1603BA987687E196E69B4
```

### 功能重點

- **任務管理**：新增／編輯／開始／完成／刪除，四色儀表板（全部／進行中／已逾期／已完成）點擊即篩選。
- **期限提醒**：可設多個提前提醒門檻；到期、逾期與錯過的門檻會合併補發；系統匣常駐＋置頂提醒視窗。
- **批量導入**：下載 Excel（.xlsx）模板，填好一次匯入，逐列檢查。
- **自動備份**：預設每 24 小時備份、保留最近 10 份，可從備份清單直接還原；清理前自動完整備份。
- **介面**：繁體中文／简体中文／English 即時切換；白天／夜間主題（可依時間自動切換，19:00 夜間、07:00 白天）；80%～150% 縮放。
- **為愛發電**：完全自願的贊助入口，只顯示本機微信／支付寶收款碼；不扣款、不驗證付款、不提供功能解鎖。

### 隱私與網路行為

- 程式沒有匿名統計、安裝 ID 或每日心跳，不會上傳任務內容或使用行為。
- 更新檢查只讀取公開版本清單（官方網站 → jsDelivr 鏡像 → GitHub 原始檔），不下載或安裝新版，也不會送出任務資料。
- 為愛發電只讀取本機或內嵌收款碼，不上傳金額、收款碼或付款結果。
- 問題回報只在使用者按下「開啟郵件程式」時把 `mailto:` 交給系統郵件程式。

### 第一次啟動與資料位置

- 任務資料預設放在 `E:\WorkTaskTrackerData\<Windows使用者名稱>\tasks.json`。
- 沒有 E 槽時會請你選擇本機資料夾；可在偏好設定「更改資料位置」搬移或切換。
- 資料路徑記在 `%LOCALAPPDATA%\WorkTaskTracker\data-directory.txt`。
- 不要把資料放在網路磁碟或同步資料夾。

---

## 简体中文

Windows 桌面任务／待办追踪工具，**只提供免安装版**：单一自包含 `WorkTaskTracker.exe`，双击即可使用，不需要安装、不需要管理员权限，也不需要另外安装 .NET Runtime。

- 当前版本：**1.0.0**（首个公开版本，文件版本 1.0.0.0）
- 系统需求：Windows 10 / Windows 11（x64）
- 数据：单机 `tasks.json`，没有数据库、没有账号系统、不上传任务内容

### 下载

| 文件 | 说明 | 大小 |
| --- | --- | --- |
| [WorkTaskTracker-1.0.0-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.0.0/WorkTaskTracker-1.0.0-portable-win-x64.zip) | **唯一需要下载的文件**。解压后只有 EXE（收款码、使用手册与发布设置都已内嵌）与使用手册，共 2 个文件 | 70,935,072 bytes |

SHA-256 与繁体中文段落相同。

### 功能重点

- **任务管理**：新增／编辑／开始／完成／删除，四色仪表板（全部／进行中／已逾期／已完成）点击即筛选。
- **期限提醒**：可设多个提前提醒门槛；到期、逾期与错过的门槛会合并补发；系统托盘常驻＋置顶提醒窗口。
- **批量导入**：下载 Excel（.xlsx）模板，填好一次导入，逐行检查。
- **自动备份**：默认每 24 小时备份、保留最近 10 份，可从备份列表直接还原；清理前自动完整备份。
- **界面**：繁体中文／简体中文／English 即时切换；白天／夜间主题（可依时间自动切换，19:00 夜间、07:00 白天）；80%～150% 缩放。
- **为爱发电**：完全自愿的赞助入口，只显示本机微信／支付宝收款码；不扣款、不验证付款、不提供功能解锁。

### 隐私与网络行为

- 程序没有匿名统计、安装 ID 或后台心跳，不会上传任务内容或使用行为。
- 更新检查只读取公开版本列表（官方网站 → jsDelivr 镜像 → GitHub 原始文件），不下载或安装新版，也不会发送任务数据。
- 为爱发电只读取本机或内嵌收款码，不上传金额、收款码或付款结果。
- 问题回报只在用户按下「打开邮件程序」时把 `mailto:` 交给系统邮件程序。

### 首次启动与数据位置

- 任务数据默认放在 `E:\WorkTaskTrackerData\<Windows用户名>\tasks.json`。
- 没有 E 盘时会请你选择本机文件夹；可在偏好设置「更改数据位置」搬移或切换。
- 数据路径记录在 `%LOCALAPPDATA%\WorkTaskTracker\data-directory.txt`。
- 不要把数据放在网络磁盘或同步文件夹。

---

## English

A portable, offline-first Windows desktop task tracker. **Portable only**: a single self-contained `WorkTaskTracker.exe`, no installation, no admin rights and no separate .NET Runtime.

- Current version: **1.0.0** (first public release, file version 1.0.0.0)
- Requirements: Windows 10 / 11 x64
- Data: local `tasks.json`; no database, no account, no task-content upload

### Download

| File | Notes | Size |
| --- | --- | --- |
| [WorkTaskTracker-1.0.0-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.0.0/WorkTaskTracker-1.0.0-portable-win-x64.zip) | **The only file you need**. Unzip to get the EXE (payment codes, manual and release settings embedded) and the manual — 2 files total | 70,935,072 bytes |

SHA-256 values are the same as in the Traditional Chinese section.

### Feature highlights

- **Task management**: add / edit / start / complete / delete, with a four-colour dashboard (all / in progress / overdue / completed) that filters on click.
- **Deadline reminders**: multiple advance thresholds per task; missed thresholds are merged and replayed; tray resident + always-on-top reminder window.
- **Batch import**: download an Excel (.xlsx) template, fill it in and import once — every row is validated.
- **Automatic backups**: every 24 hours by default, keeping the last 10; restore directly from the backup list; full backup before any cleanup.
- **Interface**: Traditional Chinese / Simplified Chinese / English with instant switching; light / dark themes (or automatic by time — dark at 19:00, light at 07:00); 80%–150% zoom.
- **Donate with Love**: a purely voluntary sponsorship entry showing local WeChat / Alipay payment codes; no charges, no payment verification, nothing locked.

### Privacy and network behaviour

- No anonymous statistics, install ID or background heartbeat; task content and usage are never uploaded.
- Update checks only read a public version list (official site → jsDelivr mirror → GitHub raw); no download or install of new versions, and no task data is sent.
- Donation only reads local or embedded payment codes; amounts, codes and payment results are never uploaded.
- Feedback only hands a `mailto:` link to your own mail app when you press the button.

### First launch and data location

- Task data defaults to `E:\WorkTaskTrackerData\<Windows user name>\tasks.json`.
- Without an E: drive the app asks you to pick a local folder; move it anytime via Preferences → "Change data location".
- The path is recorded in `%LOCALAPPDATA%\WorkTaskTracker\data-directory.txt`.
- Do not put the data on network drives or synced folders.
