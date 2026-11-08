# 工作任務追蹤 WorkTaskTracker · 工作任务追踪 · Windows Task Tracker

[繁體中文](#繁體中文) ｜ [简体中文](#简体中文) ｜ [English](#english)

**下載 Download 下载：<https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/latest>**

Windows 桌面待辦／任務追蹤工具（免安裝、離線優先、無帳號系統）／Windows 桌面待办与任务追踪工具（免安装、离线优先、无账号系统）／A portable, offline-first Windows desktop task and to-do tracker (no installation, no account, single EXE).

---

## 繁體中文

Windows 桌面待辦／任務追蹤工具，**只提供免安裝版**：單一自包含 `WorkTaskTracker.exe`，雙擊即可使用，不需要安裝、不需要管理員權限，也不需要另外安裝 .NET Runtime。

- 目前版本：**1.7.2**（檔案版本 1.7.2.0）
- 系統需求：Windows 10 / Windows 11（x64）
- 資料：單機 `tasks.json`，沒有資料庫、沒有帳號系統、不上傳任務內容

> 這個儲存庫只放**免安裝程式與使用說明**。原始碼為私有，不在這裡公開。

### 下載

| 檔案 | 說明 | 大小 |
| --- | --- | --- |
| [WorkTaskTracker-1.7.2-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.7.2/WorkTaskTracker-1.7.2-portable-win-x64.zip) | **唯一需要下載的檔案**。解壓後只有 EXE（收款碼、使用手冊與發佈設定都已內嵌）與使用手冊，共 2 個檔案 | 70,873,379 bytes |

下載 ZIP → 解壓到任意資料夾 → 雙擊 `WorkTaskTracker.exe`。任務資料與程式資料夾分開，換版或搬移程式都不影響任務資料。

### 校驗碼（SHA-256）

```text
WorkTaskTracker-1.7.2-portable-win-x64.zip
E19A01931A56D870DC6B156C04D0C1A72EA06DB5E792C800EC6DDB700D5BA3A2

WorkTaskTracker.exe
62B3B1CBCD6E90E634095EFAA0595B512850A7E67376F95B15E2BB00D97EA167

使用手冊.html
92A0C3AA27F646869BA81854D0AFB6C43CE29B849956436422A70B254B114BF4
```

### 1.7.2 重點

- **狀態篩選不再被滑鼠「滑過」誤觸**：把游標停在下拉選項上（停多久都一樣，過程中程式在背景自動刷新也不會）都不會再自己換篩選；只有真的點下去（或按 Enter）才套用，按 Esc 或點別處關閉則維持原本的篩選。同時修掉兩個成因：背景每 15 秒的到期檢查會在清單展開時重建清單，以及原生下拉「游標經過就改目前選取」。
- 回歸測試 97 項全過，包含「清單展開期間刷新不得變動清單」與「游標停在清單上關閉必須套用篩選」。

### 隱私與網路行為

- 程式沒有匿名統計、安裝 ID 或每日心跳，不會上傳任務內容或使用行為。
- 更新檢查只 GET 公開版本清單（預設優先 jsDelivr 鏡像），不下載或安裝新版，也不會送出任務資料。
- 友情贊助只讀取本機或內嵌收款碼，不上傳金額、收款碼或付款結果。
- 問題回報只在使用者按下「開啟郵件程式」時把 `mailto:` 交給系統郵件程式。

### 第一次啟動與資料位置

- 任務資料預設放在 `E:\WorkTaskTrackerData\<Windows使用者名稱>\tasks.json`。
- 沒有 E 槽時會請你選擇本機資料夾；可在偏好設定「更改資料位置」搬移或切換。
- 資料路徑記在 `%LOCALAPPDATA%\WorkTaskTracker\data-directory.txt`。
- 不要把資料放在網路磁碟或同步資料夾。

---

## 简体中文

Windows 桌面待办／任务追踪工具，**只提供免安装版**：单一自包含 `WorkTaskTracker.exe`，双击即可使用，不需要安装、不需要管理员权限，也不需要另外安装 .NET Runtime。

- 当前版本：**1.7.2**（文件版本 1.7.2.0）
- 系统需求：Windows 10 / Windows 11（x64）
- 数据：单机 `tasks.json`，没有数据库、没有账号系统、不上传任务内容

### 下载

| 文件 | 说明 | 大小 |
| --- | --- | --- |
| [WorkTaskTracker-1.7.2-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.7.2/WorkTaskTracker-1.7.2-portable-win-x64.zip) | **唯一需要下载的文件**。解压后只有 EXE（收款码、使用手册与发布设置都已内嵌）与使用手册，共 2 个文件 | 70,873,379 bytes |

SHA-256 与繁体中文段落相同。

### 1.7.2 重点

- **状态筛选不再被鼠标"滑过"误触**：把光标停在下拉选项上（停多久都一样，期间程序在后台自动刷新也不会）都不会再自己换筛选；只有真正点下去（或按 Enter）才应用，按 Esc 或点别处关闭则保持原来的筛选。同时修掉两个成因：后台每 15 秒的到期检查会在清单展开时重建清单，以及原生下拉「光标经过就改当前选中」。
- 回归测试 97 项全过，包含「清单展开期间刷新不得变动清单」与「光标停在清单上关闭必须应用筛选」。

### 隐私

- 没有匿名统计、安装 ID 或后台心跳；更新检查只读取公开版本列表；赞助与问题回报都不上传任务内容。

---

## English

A portable, offline-first Windows desktop task tracker. **Portable only**: a single self-contained `WorkTaskTracker.exe`, no installation, no admin rights and no separate .NET Runtime.

- Current version: **1.7.2** (file version 1.7.2.0)
- Requirements: Windows 10 / 11 x64
- Data: local `tasks.json`; no database, no account, no task-content upload

### Download

| File | Notes | Size |
| --- | --- | --- |
| [WorkTaskTracker-1.7.2-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.7.2/WorkTaskTracker-1.7.2-portable-win-x64.zip) | **The only file you need**. Unzip to get the EXE (payment codes, manual and release settings embedded) and the manual — 2 files total | 70,873,379 bytes |

SHA-256 values are the same as in the Traditional Chinese section.

### What's new in 1.7.2

- **The status filter can no longer be applied by hovering**: resting the pointer on a dropdown item — for any amount of time, and even while the app refreshes in the background — no longer changes the filter. Only a real click (or Enter) applies it; Esc, or closing the list somewhere else, keeps the previous choice. Two root causes are fixed: the 15-second reminder poll rebuilt the grid while the list was open, and the native combo box moves the selection as the pointer passes over items.
- All 97 regression tests pass, including "a refresh while the list is open must not change the list" and "closing with the pointer over the list must apply the pick".

### Privacy

- No anonymous statistics, install ID or background heartbeat.
- Update checks only read a public version list; no task content is sent.
- Sponsorship only reads local or embedded payment codes; nothing is uploaded.
- Feedback only hands a `mailto:` link to your own mail app when you press the button.
