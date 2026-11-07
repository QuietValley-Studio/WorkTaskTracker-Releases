# 工作任務追蹤 WorkTaskTracker · 工作任务追踪 · Windows Task Tracker

[繁體中文](#繁體中文) ｜ [简体中文](#简体中文) ｜ [English](#english)

**下載 Download 下载：<https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/latest>**

Windows 桌面待辦／任務追蹤工具（免安裝、離線優先、無帳號系統）／Windows 桌面待办与任务追踪工具（免安装、离线优先、无账号系统）／A portable, offline-first Windows desktop task and to-do tracker (no installation, no account, single EXE).

---

## 繁體中文

Windows 桌面待辦／任務追蹤工具，**只提供免安裝版**：單一自包含 `WorkTaskTracker.exe`，雙擊即可使用，不需要安裝、不需要管理員權限，也不需要另外安裝 .NET Runtime。

- 目前版本：**1.7.0**（檔案版本 1.7.0.0）
- 系統需求：Windows 10 / Windows 11（x64）
- 資料：單機 `tasks.json`，沒有資料庫、沒有帳號系統、不上傳任務內容

> 這個儲存庫只放**免安裝程式與使用說明**。原始碼為私有，不在這裡公開。

### 下載

| 檔案 | 說明 | 大小 |
| --- | --- | --- |
| [WorkTaskTracker-1.7.0-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.7.0/WorkTaskTracker-1.7.0-portable-win-x64.zip) | **唯一需要下載的檔案**。解壓後只有 EXE（收款碼、使用手冊與發佈設定都已內嵌）與使用手冊，共 2 個檔案 | 70,700,746 bytes |

下載 ZIP → 解壓到任意資料夾 → 雙擊 `WorkTaskTracker.exe`。任務資料與程式資料夾分開，換版或搬移程式都不影響任務資料。

### 校驗碼（SHA-256）

```text
WorkTaskTracker-1.7.0-portable-win-x64.zip
4BCF8AA9844F7DA2D76DEC08A1707C3C05AEBBEE129D0A3FFCA879DA51878FD5

WorkTaskTracker.exe
78BDF18707AF419A5955E0ECDC7AD4D3A76E30ABA27D0C4C12EA4FB8FB01BD59

使用手冊.html
5BFA1A43548748FC5E7B772168BE5B94364C0655ACCFF07EADE2095C9BAD5721
```

### 1.7.0 重點

- **全站 QQ 風格配色**：白天 QQ 藍＋淺灰工作台＋白卡片；夜間近黑底＋深灰卡片；按鈕、統計卡、下拉、狀態標籤、進度條、提醒卡與列內操作統一。
- **移除匿名使用統計**：不再有安裝 ID、統計端點或背景心跳；只保留檢查更新讀取公開版本清單。
- **檢查更新修正**：預設改用 jsDelivr 鏡像優先、官方來源次之；失敗時顯示實際原因。
- **彈窗動畫**：開啟淡入＋上滑、關閉淡出＋下滑；修正首次啟動整片半透明的問題。
- **下拉選單重寫**：字級與列高加大、箭頭區加大；離屏快取並停止 hover 重繪，消除閃爍。
- **提醒輸入友善化**：常用 1 天／1 小時／30 分／15 分／5 分膠囊多選＋自訂分鐘。
- **可更改資料位置**：新位置已有資料會詢問是否直接改用；空白則詢問是否複製目前資料。
- **CSV 批量導入**：下載模板、選檔、預覽與逐列錯誤提示，整批成功才寫入。
- **備份視窗修正**：加寬並改等寬按鈕，避免文字與按鈕截斷；底部摘要區縮小。

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

- 当前版本：**1.7.0**（文件版本 1.7.0.0）
- 系统需求：Windows 10 / Windows 11（x64）
- 数据：单机 `tasks.json`，没有数据库、没有账号系统、不上传任务内容

### 下载

| 文件 | 说明 | 大小 |
| --- | --- | --- |
| [WorkTaskTracker-1.7.0-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.7.0/WorkTaskTracker-1.7.0-portable-win-x64.zip) | **唯一需要下载的文件**。解压后只有 EXE（收款码、使用手册与发布设置都已内嵌）与使用手册，共 2 个文件 | 70,700,746 bytes |

SHA-256 与繁体中文段落相同。

### 1.7.0 重点

- **全站 QQ 风格配色**：白天 QQ 蓝＋浅灰工作台＋白卡片；夜间近黑底＋深灰卡片；按钮、统计卡、下拉、状态标签、进度条、提醒卡与行内操作统一。
- **移除匿名使用统计**；**检查更新改用镜像优先**；**弹窗开启/关闭淡入淡出**并修正首次启动半透明。
- **下拉选单重写**：字体与列高加大、消除箭头闪烁；**提醒改常用胶囊＋自定义分钟**。
- **可更改数据位置**：新位置已有数据会询问是否直接改用，空白则询问是否复制。
- **CSV 批量导入**（模板下载、预览、逐列错误）；**备份窗口加宽**避免截断；底部摘要缩小。

### 隐私

- 没有匿名统计、安装 ID 或后台心跳；更新检查只读取公开版本列表；赞助与问题回报都不上传任务内容。

---

## English

A portable, offline-first Windows desktop task tracker. **Portable only**: a single self-contained `WorkTaskTracker.exe`, no installation, no admin rights and no separate .NET Runtime.

- Current version: **1.7.0** (file version 1.7.0.0)
- Requirements: Windows 10 / 11 x64
- Data: local `tasks.json`; no database, no account, no task-content upload

### Download

| File | Notes | Size |
| --- | --- | --- |
| [WorkTaskTracker-1.7.0-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.7.0/WorkTaskTracker-1.7.0-portable-win-x64.zip) | **The only file you need**. Unzip to get the EXE (payment codes, manual and release settings embedded) and the manual — 2 files total | 70,700,746 bytes |

SHA-256 values are the same as in the Traditional Chinese section.

### What's new in 1.7.0

- **QQ-style palette for light and dark themes**: QQ blue accent, light gray workspace and white cards in light mode; near-black background and dark cards at night. Buttons, stat cards, dropdowns, status pills, progress bars, reminder cards and row actions all follow the same palette.
- **Anonymous usage reporting removed**; **update checks prefer the jsDelivr mirror** and show the real failure reason.
- **Open/close popup animations** (fade + slide) and a fix for the first-launch translucent window.
- **Rewritten dropdowns** with larger text, no hover flicker; **friendly reminder presets + custom minutes**.
- **Change data location** with copy / detect-manual-move prompts; **CSV batch import** with template, preview and row errors; **wider backup dialog**; **compact bottom summary**.

### Privacy

- No anonymous statistics, install ID or background heartbeat.
- Update checks only read a public version list; no task content is sent.
- Sponsorship only reads local or embedded payment codes; nothing is uploaded.
- Feedback only hands a `mailto:` link to your own mail app when you press the button.