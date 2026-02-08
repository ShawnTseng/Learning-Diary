# Channels 頁面完整教學 📡

## 🎯 Channels 是什麼？

**Channels = 通訊管道**

讓你可以透過不同平台跟我互動：
- Telegram（已設定 ✅）
- WhatsApp
- Discord
- Slack
- Signal
- iMessage
- Google Chat

---

## 📱 目前已啟用：Telegram

**狀態：** ✅ ON  
**Bot：** @ShawnTseng_bot  
**你的帳號：** @dao0x2n1k5 (ID: 1036407055)

---

## 🔧 Telegram 設定詳解

在 Channels 頁面，你會看到 Telegram 設定區塊：

### 1️⃣ **Enabled（啟用開關）**
- ✅ ON = Telegram bot 運作中
- ❌ OFF = 關閉 Telegram 功能

---

### 2️⃣ **Bot Token（機器人 Token）**
```
8399******xfak
```
- 從 BotFather 取得的 token
- 用來驗證 bot 身份
- **不要分享給別人！**

**已設定，不用改！**

---

### 3️⃣ **DM Policy（私訊政策）**

**目前設定：pairing（配對模式）**

**三種模式：**

| 模式 | 說明 | 適用情境 |
|------|------|----------|
| **pairing** ⭐ | 需要批准才能用 | 只有你一個人用（安全） |
| **allowlist** | 白名單制（填 allowFrom） | 固定幾個人用 |
| **open** | 任何人都能用 | 公開 bot（危險！） |

**建議：** 保持 `pairing` 模式

---

### 4️⃣ **allowFrom（白名單）**

**用途：** 指定誰可以直接使用（不用配對）

**填寫方式：**
```
@dao0x2n1k5
```
或
```
1036407055
```

**如果填了：**
- 這些人可以直接跟我聊天
- 不用等你批准

**如果不填：**
- 每個新用戶都要你手動批准（像之前一樣）

**建議：**
- 如果只有你用 → 填 `@dao0x2n1k5`
- 如果可能有其他人 → 不填，維持配對模式

---

### 5️⃣ **Group Policy（群組政策）**

**目前設定：allowlist（白名單）**

**三種模式：**

| 模式 | 說明 | 適用情境 |
|------|------|----------|
| **allowlist** ⭐ | 只有白名單群組能用 | 控制哪些群組可以加我 |
| **open** | 任何群組都能加 | 公開使用 |
| **deny** | 禁止所有群組 | 只允許私訊 |

**allowlist 設定：**
需要填寫「允許的群組 ID」

**範例：**
```
-1001234567890
```

**如何取得群組 ID：**
1. 把我加入群組
2. 我會告訴你群組 ID
3. 到 Channels 設定填入

---

### 6️⃣ **Stream Mode（串流模式）**

**目前設定：partial（部分串流）**

**三種模式：**

| 模式 | 說明 | 體驗 |
|------|------|------|
| **off** | 不串流，等回覆完成才送出 | 看到完整訊息 |
| **partial** ⭐ | 部分串流，分段送出 | 即時看到回覆（推薦） |
| **full** | 完整串流，逐字送出 | 像打字機一樣 |

**建議：** 保持 `partial`（平衡速度與體驗）

---

### 7️⃣ **Reactions（反應模式）**

**設定：** MINIMAL（最小化）

**模式說明：**
- **MINIMAL** - 只在重要時才 react（👍、❤️ 等）
- **NORMAL** - 正常頻率 react
- **OFF** - 不使用 emoji 反應

**目前設定：**
大約每 5-10 則訊息才會 react 一次

---

### 8️⃣ **Reply Mode（回覆模式）**

**設定：** 自動偵測

**功能：**
- 在 Telegram 回覆時會「引用」你的訊息
- 讓對話更清楚

---

### 9️⃣ **Pairing List（配對清單）**

**查看已配對的用戶：**
- 你的帳號：@dao0x2n1k5 (1036407055)
- 配對時間：2026-02-08
- 配對碼：32WJNSUJ

**操作：**
- **Approve** - 批准新用戶
- **Reject** - 拒絕請求
- **Remove** - 移除已配對用戶

---

### 🔟 **Test Connection（測試連線）**

**按鈕功能：**
- 點「Test」→ 發送測試訊息到 Telegram
- 確認 bot 是否正常運作

**如果測試失敗：**
1. 檢查 Bot Token 是否正確
2. 檢查網路連線
3. 到終端機執行 `openclaw status --deep`

---

## 🆕 新增其他 Channels

### 📱 WhatsApp

**設定步驟：**
1. Channels 頁面點「Add Channel」
2. 選擇「WhatsApp」
3. 掃描 QR Code
4. 完成配對

**功能：**
- 跟 Telegram 一樣
- 支援群組
- 支援語音訊息

---

### 💬 Discord

**設定步驟：**
1. 建立 Discord Bot（Discord Developer Portal）
2. 取得 Bot Token
3. 在 Channels 頁面填入 Token
4. 邀請 bot 到伺服器

**功能：**
- 支援多伺服器
- 支援頻道管理
- 支援角色權限

---

### 📧 Slack

**設定步驟：**
1. 建立 Slack App
2. 取得 Bot Token
3. 填入 Channels 設定
4. 安裝到 workspace

---

### 🔔 Signal

**設定步驟：**
1. 需要額外設定 Signal CLI
2. 比較技術向
3. 適合重視隱私的用戶

---

### 💬 iMessage（僅 macOS）

**設定步驟：**
1. 需要 macOS 系統
2. 開啟「訊息」app 權限
3. 在 Channels 啟用

**限制：**
- 僅 Mac 可用
- 需要系統權限

---

## 🎯 實用場景

### 場景 1：只用 Telegram
**設定：**
- DM Policy: `pairing`
- allowFrom: `@dao0x2n1k5`
- Group Policy: `deny`（禁止群組）

**結果：**
只有你能私訊我，不會被陌生人打擾

---

### 場景 2：允許家人使用
**設定：**
- DM Policy: `allowlist`
- allowFrom: 
  ```
  @dao0x2n1k5
  @family_member_1
  @family_member_2
  ```

**結果：**
你和家人都能直接使用

---

### 場景 3：團隊協作（群組）
**設定：**
- Group Policy: `allowlist`
- 允許的群組 ID：
  ```
  -1001234567890
  -1009876543210
  ```

**結果：**
特定群組可以使用我的功能

---

## ⚠️ 安全建議

### ❌ 不建議的設定
- DM Policy = `open`（任何人都能用）
- Group Policy = `open`（任何群組都能加）
- 分享 Bot Token

### ✅ 建議的設定
- DM Policy = `pairing` 或 `allowlist`
- 定期檢查配對清單
- 移除不認識的用戶
- 保管好 Bot Token

---

## 🔍 常見問題

### Q: Telegram 訊息沒收到？
**檢查：**
1. Bot Token 是否正確
2. 是否已配對
3. 點「Test Connection」測試

### Q: 如何移除已配對用戶？
**步驟：**
1. Channels → Telegram
2. Pairing List 找到該用戶
3. 點「Remove」

### Q: 如何新增白名單？
**步驟：**
1. DM Policy 改成 `allowlist`
2. 填寫 allowFrom（username 或 user ID）
3. Save

### Q: 群組 ID 怎麼取得？
**方法 1：**
- 把我加入群組
- 我會回報群組 ID

**方法 2：**
- 用 bot 如 @userinfobot
- 轉發群組訊息給它

---

## 📊 Channels 頁面操作總覽

**查看狀態：**
- ✅ 綠色勾勾 = 正常運作
- ❌ 紅色叉叉 = 連線失敗

**常用按鈕：**
- **Enable/Disable** - 開關 channel
- **Test** - 測試連線
- **Save** - 儲存設定
- **Refresh** - 刷新狀態

**進階功能：**
- **Logs** - 查看訊息記錄
- **Stats** - 查看使用統計
- **Export** - 匯出設定

---

**Channels 就是你跟我互動的「橋樑」！** 🌉

目前用 Telegram 就很夠了，之後有需要再加其他平台！

**有問題隨時問！** 📣
