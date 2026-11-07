# 工作任務追蹤 WorkTaskTracker · 工作任务追踪 · Windows Task Tracker

[繁體中文](#繁體中文) ｜ [简体中文](#简体中文) ｜ [English](#english)

**下載 Download 下载：<https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/latest>**

Windows 桌面待辦／任務追蹤工具（免安裝、離線優先、無帳號系統）／Windows 桌面待办与任务追踪工具（免安装、离线优先、无账号系统）／A portable, offline-first Windows desktop task and to-do tracker (no installation, no account, single EXE).

---

## 繁體中文

Windows 桌面待辦／任務追蹤工具，**只提供免安裝版**：單一自包含 `WorkTaskTracker.exe`，雙擊即可使用，不需要安裝、不需要管理員權限，也不需要另外安裝 .NET Runtime。

- 目前版本：**1.7.1**（檔案版本 1.7.1.0）
- 系統需求：Windows 10 / Windows 11（x64）
- 資料：單機 `tasks.json`，沒有資料庫、沒有帳號系統、不上傳任務內容

> 這個儲存庫只放**免安裝程式與使用說明**。原始碼為私有，不在這裡公開。

### 下載

| 檔案 | 說明 | 大小 |
| --- | --- | --- |
| [WorkTaskTracker-1.7.1-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.7.1/WorkTaskTracker-1.7.1-portable-win-x64.zip) | **唯一需要下載的檔案**。解壓後只有 EXE（收款碼、使用手冊與發佈設定都已內嵌）與使用手冊，共 2 個檔案 | 70,643,441 bytes |

下載 ZIP → 解壓到任意資料夾 → 雙擊 `WorkTaskTracker.exe`。任務資料與程式資料夾分開，換版或搬移程式都不影響任務資料。

### 校驗碼（SHA-256）

```text
WorkTaskTracker-1.7.1-portable-win-x64.zip
5F6801FDF483ED1EE97C87FC68D6E4B2DCC6C41BF753049FE81D2C24D4BDA032

WorkTaskTracker.exe
8FD72CCDBD621402B8E6A6D24F02295B9AD286F4D15F5622321309A852DF30D0

使用手冊.html
865D00EA89A33EB692444A04C7FAB292FFFBB93281796B237B84CE4EFC7D8877
```

### 1.7.1 重點

- **任務清單瘦身並自動撐滿寬度**：刪除「刪除」之後的專案、預計完成、預估工時與各時間戳記欄位（資料仍完整保留在 `tasks.json`，只是不再佔版面）；最前面新增「序號」欄，永遠從 1 遞增；「備註」欄移到操作按鈕前面，一眼看完再決定動作。
- **四張統計卡四種顏色**：未結束＝藍、進行中＝琥珀、已逾期＝紅、已完成＝青，卡片底色與邊框也依顏色淡淡染色，不必讀文字就能分辨。
- **表頭按鈕分成左右兩組**：使用手冊與「＋ 新增任務」靠左，「問題回報」與「友情贊助」靠右；友情贊助按鈕加上緩慢呼吸的高光（約 2.3 秒一循環），只是提示入口存在，不搶主按鈕。
- **專案／分類改為「先建立、後挑選」**：任務編輯視窗的下拉選單不再接受輸入，第一項固定「未分類」，要新增選項得按「管理選項」；管理視窗改成卡片式（輸入名稱→按加入→出現小卡片，點卡片上的 × 移除），與提前提醒的操作方式一致。
- **批量導入視窗**：移除沒有作用的錯誤文字框，視窗改為依內容自動調整高度，說明與錯誤訊息變多時自己長高，不再出現垂直捲軸。
- **篩選只認真的點選**：把滑鼠停在下拉選項上不會再自己換篩選，清單被外力關閉時也會還原；篩選項目改名為「未結束（含未開始）」，欄寬依文字實測，不再出現「未結束（含未開…」。
- **其他修復**：時程分頁「加入提醒」的單位下拉選單邊框消失；下拉選單重寫繪製層（換值立刻反映、滑鼠移入不再閃）；彈窗關閉不再讓後方視窗閃一下；側欄底色由暖米白改為近白。

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

- 当前版本：**1.7.1**（文件版本 1.7.1.0）
- 系统需求：Windows 10 / Windows 11（x64）
- 数据：单机 `tasks.json`，没有数据库、没有账号系统、不上传任务内容

### 下载

| 文件 | 说明 | 大小 |
| --- | --- | --- |
| [WorkTaskTracker-1.7.1-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.7.1/WorkTaskTracker-1.7.1-portable-win-x64.zip) | **唯一需要下载的文件**。解压后只有 EXE（收款码、使用手册与发布设置都已内嵌）与使用手册，共 2 个文件 | 70,643,441 bytes |

SHA-256 与繁体中文段落相同。

### 1.7.1 重点

- **任务清单精简并自动撑满宽度**：删除「删除」之后的项目、预计完成、预估工时与各时间戳字段（数据仍完整保存在 `tasks.json`）；最前面新增「序号」列，永远从 1 递增；「备注」列移到操作按钮前。
- **四张统计卡四种颜色**：未结束＝蓝、进行中＝琥珀、已逾期＝红、已完成＝青，卡片底色与边框也按颜色淡淡染色。
- **表头按钮分左右两组**：使用手册与「＋ 新增任务」靠左，问题回馈与友情赞助靠右；友情赞助按钮加上缓慢呼吸的高光。
- **项目／分类改为「先建立、后挑选」**：编辑窗口的下拉不再接受输入，管理窗口改为卡片式（输入→加入→出现卡片，点 × 移除）。
- **批量导入窗口**：移除无用的错误文本框，改为按内容自动调整高度，不再出现滚动条。
- **筛选只认真正的点选**：鼠标滑过下拉选项不会再自动换筛选；项目改名为「未结束（含未开始）」。
- **其他修复**：加入提醒的单位下拉边框消失；下拉菜单重写绘制层；关闭弹窗不再让后面窗口闪一下；侧栏底色改为近白。

### 隐私

- 没有匿名统计、安装 ID 或后台心跳；更新检查只读取公开版本列表；赞助与问题回报都不上传任务内容。

---

## English

A portable, offline-first Windows desktop task tracker. **Portable only**: a single self-contained `WorkTaskTracker.exe`, no installation, no admin rights and no separate .NET Runtime.

- Current version: **1.7.1** (file version 1.7.1.0)
- Requirements: Windows 10 / 11 x64
- Data: local `tasks.json`; no database, no account, no task-content upload

### Download

| File | Notes | Size |
| --- | --- | --- |
| [WorkTaskTracker-1.7.1-portable-win-x64.zip](https://github.com/QuietValley-Studio/WorkTaskTracker-Releases/releases/download/v1.7.1/WorkTaskTracker-1.7.1-portable-win-x64.zip) | **The only file you need**. Unzip to get the EXE (payment codes, manual and release settings embedded) and the manual — 2 files total | 70,643,441 bytes |

SHA-256 values are the same as in the Traditional Chinese section.

### What's new in 1.7.1

- **A leaner task list that fills the card**: every column after the delete action (project, expected date, estimated hours, timestamps) is gone from the grid — the data stays in `tasks.json`; a new `#` column counts from 1; the notes column moved in front of the row actions.
- **Four distinct stat-card colours**: open = blue, in progress = amber, overdue = red, completed = teal, with tinted fills and borders so you can tell them apart without reading.
- **Header buttons split into two groups**: manual and “+ New task” on the left, feedback and sponsor on the right; the sponsor button breathes slowly (~2.3 s cycle) so the entry point is noticeable without stealing focus.
- **Categories are create-first, then pick**: the editor dropdown is read-only and starts with “未分類” (uncategorised); the manager is now chip-based (type → add → chip appears, click × to remove), matching the reminder editor.
- **Import dialog** sizes itself to its content — the dead error text box is gone and long notes no longer force a scrollbar.
- **The status filter only applies a real pick**: hovering an item no longer changes the filter, and an externally closed list restores the previous choice; the first entry is now “未結束（含未開始）” (open, including not started).
- **Fixes**: missing border on the reminder unit dropdown, a repainted dropdown layer (instant value changes, no hover flicker), no more flash on the window behind a closing dialog, and a near-white sidebar.

### Privacy

- No anonymous statistics, install ID or background heartbeat.
- Update checks only read a public version list; no task content is sent.
- Sponsorship only reads local or embedded payment codes; nothing is uploaded.
- Feedback only hands a `mailto:` link to your own mail app when you press the button.
