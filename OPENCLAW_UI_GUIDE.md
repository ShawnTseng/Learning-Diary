# OpenClaw Dashboard 學習指南 🎓

## 🎯 Dashboard 完整導覽

**Dashboard 位址：** http://127.0.0.1:18789/

**初次登入：**
1. 右上角 Settings (⚙️)
2. 找到「Gateway Token」
3. 貼上：`e22a79d73cb8d3d1dbb6a644a83184f2465711077a7602ff`
4. Save（瀏覽器會記住）

---

## 📑 主要頁面功能

### 1️⃣ **Overview（總覽）** 🏠
**位置：** 左側選單第一個

**功能：**
- ✅ 系統狀態一覽
- ✅ Gateway 連線狀態
- ✅ Channel 狀態（Telegram 等）
- ✅ 快速診斷資訊

**你會看到：**
- Dashboard URL
- OS 版本
- Gateway 狀態
- Telegram 連接狀態
- Session 列表

---

### 2️⃣ **Chat（對話）** 💬
**位置：** 左側選單第二個

**功能：**
- ✅ 直接跟我聊天（就像 Telegram 一樣）
- ✅ 看到完整對話記錄
- ✅ 測試指令和功能
- ✅ 查看我的回應細節

**特色：**
- 支援 Markdown 格式
- 可以上傳檔案
- Shift+Enter 換行，Enter 送出

---

### 3️⃣ **Sessions（會話管理）** 🧵
**位置：** 左側選單「Sessions」

**功能：**
- ✅ 查看所有對話 session
- ✅ 切換不同 session
- ✅ 查看 token 使用量
- ✅ 管理 sub-agent（子代理）

**會看到：**
- Session Key（識別碼）
- 使用的模型（Claude Sonnet 4.5）
- Token 使用量（48k/128k）
- 最後活動時間

---

### 4️⃣ **Agents（代理設定）** 🤖
**位置：** 左側選單「Agents」

**功能：**
- ✅ 查看所有 agent 列表
- ✅ 建立新 agent
- ✅ 修改 agent 設定
- ✅ 設定 workspace 路徑

**可以調整：**
- Agent 名稱
- 使用的模型
- Workspace 位置
- 記憶設定

---

### 5️⃣ **Channels（通訊頻道）** 📡
**位置：** 左側選單「Channels」

**功能：**
- ✅ 管理 Telegram Bot
- ✅ 設定其他通訊平台（Discord、Slack 等）
- ✅ 配對管理（誰能用）
- ✅ 測試連線

**Telegram 設定：**
- Bot Token（已設定）
- DM Policy（配對模式）
- 白名單管理（allowFrom）
- 群組設定

---

### 6️⃣ **Skills（技能管理）** 🛠️
**位置：** 左側選單「Skills」

**功能：**
- ✅ 查看已安裝 skills
- ✅ 安裝新 skills
- ✅ 啟用/停用 skills
- ✅ 更新 skills

**目前已安裝：**
- healthcheck（系統檢查）
- skill-creator（建立技能）
- weather（天氣查詢）

**可以從這裡安裝更多：**
https://clawhub.com

---

### 7️⃣ **Memory（記憶管理）** 🧠
**位置：** 左側選單「Memory」

**功能：**
- ✅ 查看記憶檔案（MEMORY.md）
- ✅ 瀏覽每日 log（memory/YYYY-MM-DD.md）
- ✅ 編輯記憶內容
- ✅ 搜尋記憶

**記憶架構：**
- `MEMORY.md` - 長期記憶（策展）
- `memory/2026-02-08.md` - 每日記錄
- `memory/archive/` - 歸檔區

---

### 8️⃣ **Cron Jobs（定時任務）** ⏰
**位置：** 左側選單「Cron」

**功能：**
- ✅ 建立定期任務
- ✅ 設定提醒
- ✅ 自動化工作流程
- ✅ 查看執行歷史

**可以設定：**
- 每日檢查 inbox
- 定時整理檔案
- 提醒事項
- 自動備份

**範例：**
```
每天早上 9:00 提醒我檢查郵件
每週日晚上 22:00 整理一週記憶
```

---

### 9️⃣ **Files（檔案瀏覽）** 📁
**位置：** 左側選單「Files」

**功能：**
- ✅ 瀏覽 workspace 檔案
- ✅ 編輯文件
- ✅ 上傳/下載檔案
- ✅ 檔案管理

**目前可看到：**
- `MEMORY.md`
- `USER.md`
- `IDENTITY.md`
- `SOUL.md`
- `KNOWLEDGE_MANAGEMENT.md`
- `memory/` 資料夾

---

### 🔟 **Settings（設定）** ⚙️
**位置：** 右上角齒輪圖示

**功能：**
- ✅ Gateway Token 設定
- ✅ 主題切換（深色/淺色）
- ✅ 通知設定
- ✅ 進階選項

**重要設定：**
- Gateway Token（登入用）
- Model 選擇（預設模型）
- Workspace 路徑
- Auto-save 選項

---

## 🎓 學習路徑建議

### 第一階段：基礎操作（今天）
1. ✅ **Overview** - 了解系統狀態
2. ✅ **Chat** - 試著跟我聊天
3. ✅ **Sessions** - 查看對話記錄
4. ✅ **Settings** - 設定 token

### 第二階段：進階功能（明天）
5. ✅ **Files** - 瀏覽和編輯檔案
6. ✅ **Memory** - 看看我的記憶
7. ✅ **Channels** - 調整 Telegram 設定

### 第三階段：自動化（下週）
8. ✅ **Cron Jobs** - 建立自動化任務
9. ✅ **Skills** - 安裝新功能
10. ✅ **Agents** - 建立專用 agent

---

## 💡 實用技巧

### Dashboard 快捷鍵
- `Ctrl/Cmd + K` - 快速搜尋
- `Shift + Enter` - 換行（聊天時）
- `Enter` - 送出訊息

### 常用操作
- **查看 token 使用量** → Sessions 頁面
- **編輯記憶檔案** → Memory 或 Files 頁面
- **測試 Telegram** → Channels 頁面「Test」按鈕
- **建立提醒** → Cron Jobs 頁面「New Job」

### 診斷工具
- **系統狀態異常** → Overview 頁面「Run Diagnostics」
- **連線問題** → Settings 檢查 Gateway Token
- **Telegram 不通** → Channels 檢查 Bot Token

---

## 📚 延伸學習資源

**官方文件：**
- https://docs.openclaw.ai

**社群：**
- Discord: https://discord.com/invite/clawd

**技能中心：**
- https://clawhub.com

**故障排除：**
- https://docs.openclaw.ai/troubleshooting

---

## 🚀 開始探索！

**現在就打開 Dashboard：**
http://127.0.0.1:18789/

**建議第一件事：**
1. 到 **Chat** 頁面跟我說 `hello`
2. 到 **Files** 頁面看看 workspace 檔案
3. 到 **Memory** 看看今天的記錄

**有任何問題隨時問我！** 📣

我會在 Telegram 和 Dashboard 同時回覆你 💬

---

**更新日期：** 2026-02-08  
**你的專屬 OpenClaw 學習指南** 🦞
