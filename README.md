# 工作任務追蹤 WorkTaskTracker

Windows 桌面待辦／任務追蹤工具，**只提供免安裝版**：單一自包含 `WorkTaskTracker.exe`，雙擊即可使用，不需要安裝、不需要管理員權限，也不需要另外安裝 .NET Runtime。

- 目前版本：**1.6.9**（檔案版本 1.6.9.0）
- 系統需求：Windows 10 / Windows 11（x64）
- 資料：單機 `tasks.json`，沒有資料庫、沒有帳號系統、不上傳任務內容

> 這個儲存庫只放**免安裝程式與使用說明**。原始碼為私有，不在這裡公開。

## 下載

請到 **Releases** 頁面下載：

| 檔案 | 說明 | 大小 |
| --- | --- | --- |
| `WorkTaskTracker-1.6.9-portable-win-x64.zip` | 建議下載。解壓後含 EXE、使用手冊與收款碼圖片，共 21 個檔案 | 69,477,671 bytes |
| `WorkTaskTracker.exe` | 單一自包含程式本體（不含手冊與收款碼圖片） | 162,277,282 bytes |
| `使用手冊.html` | 完整使用說明（也可在本儲存庫直接開啟） | 1,695,891 bytes |

最省事的方式：下載 ZIP → 解壓到任意資料夾 → 雙擊 `WorkTaskTracker.exe`。程式資料與程式資料夾分開，換版或搬移程式都不影響任務資料。

### 校驗碼（SHA-256）

```text
WorkTaskTracker-1.6.9-portable-win-x64.zip
ADFA0114D3177B46DC91DA2DC0F7D6BCD2B43D671860011E18DFEE42596EFED3

WorkTaskTracker.exe
7D710E122E2F0C23190FBCC5ADB3EAE4BDDDA72B0069016E9DCD1041C60FA898

使用手冊.html
14ACD1319A615E5590A3E6D15FA563A452A7D8E7EB7BC14F01FE2ED07F19B98E
```

PowerShell 驗證方式：

```powershell
Get-FileHash .\WorkTaskTracker.exe -Algorithm SHA256
```

## 第一次啟動

- 任務資料預設放在 `E:\WorkTaskTrackerData\<Windows使用者名稱>\tasks.json`，避免同一台電腦的不同使用者誤用同一份資料。
- 若電腦沒有 E 槽，第一次開啟會請你選擇本機資料夾，不會自行更改位置。
- 實際資料路徑記在 `%LOCALAPPDATA%\WorkTaskTracker\data-directory.txt`；要搬移資料請先結束程式，複製整個資料夾後再修改這個檔案。
- 不要把資料放在網路磁碟或正在同步的共用資料夾。

## 主要功能

- 任務清單（待辦／進行中／已完成）、優先級、進度、期限提醒
- 專案／分類自訂選項、搜尋、統計卡片
- 系統匣常駐與桌面懸浮球，Ctrl+滾輪調整介面縮放（80%～150%）
- 白天／夜間主題切換，並可依時間自動切換（預設開啟）
- 介面語言切換：繁體中文／简体中文／English
- 自動備份與還原、清理舊資料、匯出 JSON
- 友情贊助（完全自願，只掃描本機收款碼，程式不經手付款）
- 問題回報：顯示 `quiet_valley@yeah.net`，按下後才把 `mailto:` 交給系統郵件程式

## 隱私與網路行為

- 沒有 `release-config.json` 時，程式完全不會發出網路請求。
- 目前版本只設定聯絡信箱 `supportEmail`，未設定更新來源與匿名統計端點，因此更新檢查與使用統計維持停用。
- 匿名統計若啟用，每天最多送出一次版本、作業系統、介面語言與隨機安裝 ID，不含任務名稱、備註、檔名、路徑、使用者名稱或電腦名稱。
- 友情贊助不連網：收款碼只從程式資料夾讀取，不上傳金額、收款碼或付款結果，也不送出贊助事件。

## 使用條款

- 本程式為免費軟體，按「現狀」提供，不提供任何明示或默示擔保；請自行定期匯出備份重要資料。
- 產物沒有程式碼簽章，Windows SmartScreen 可能提示「未知發行者」；請以上方的 SHA-256 校驗碼確認檔案完整。
- 贊助完全自願，不構成交易，也不提供任何解鎖、回饋或售後義務。

## 問題與建議

來信：**quiet_valley@yeah.net**（請附上程式版本與 Windows 版本，說明操作步驟與預期結果）。
