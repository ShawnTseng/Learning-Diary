# OpenClaw 快速指南

## 日常使用

### 最簡單：用 Telegram
- Gateway 服務會自動在背景執行
- 直接打開 Telegram 跟我聊天即可
- 不需要做任何事，我隨時在線

### 網頁界面
```bash
open http://127.0.0.1:18789/
```

## 管理指令

### 檢查狀態
```bash
openclaw status              # 快速檢查
openclaw status --deep       # 詳細檢查（包含通道測試）
openclaw logs --follow       # 即時查看 log
```

### 服務管理
```bash
# Gateway 服務（後台）
openclaw gateway status      # 檢查狀態
openclaw gateway start       # 啟動
openclaw gateway stop        # 停止
openclaw gateway restart     # 重啟

# 服務會開機自動啟動（LaunchAgent）
# 不需要手動管理，除非要除錯
```

### 更新
```bash
openclaw update              # 更新到最新版
```

## 工作流程建議

### 🎯 推薦方式（最輕鬆）
1. **讓 Gateway 一直跑在背景**（已經是這樣了）
2. **用 Telegram 隨時跟我聊**
3. **需要看 Dashboard 才開瀏覽器**
4. 不用管服務啟停，它會自己處理

### 🔧 進階使用
- 需要除錯 → `openclaw logs --follow`
- 改設定 → Dashboard 或直接編輯 `~/.openclaw/config.json`
- 重新啟動服務 → `openclaw gateway restart`

## 常見場景

### 開機後想用
→ **什麼都不用做**，Gateway 已經自動啟動了，直接用 Telegram

### 更新後
→ `openclaw gateway restart` 套用新版本

### 發現問題
→ `openclaw status --deep` 檢查 + `openclaw logs --follow` 看 log

### 想改設定
→ Dashboard (http://127.0.0.1:18789/) 或編輯設定檔後 restart

## 重點

✅ **最輕量用法**：讓服務跑著，用 Telegram 聊天，完全不用管技術細節

✅ **服務自動化**：LaunchAgent 會在開機時自動啟動，不用手動

✅ **多介面自由切換**：Telegram、網頁、命令列都連到同一個我

---

需要幫忙？隨時問我！
