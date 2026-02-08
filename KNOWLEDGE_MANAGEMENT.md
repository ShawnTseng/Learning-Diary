# 知識與資料管理架構

## 🎯 核心原則

**安全第一，白名單策略**
- 只存取明確授權的資料夾與檔案
- 敏感資料需要額外加密保護
- 定期審查權限範圍

**結構化管理**
- 分類清楚、易於搜尋
- 定期整理與歸檔
- 自動化備份與版本控制

---

## 📁 資料分層架構

### Tier 0: OpenClaw Workspace（當前目錄）
**路徑：** `/Users/tsengjiyang/.openclaw/workspace`
**用途：** OpenClaw 核心資料、記憶、配置
**權限：** 完全存取

```
workspace/
├── memory/              # 日常記憶檔案
│   └── YYYY-MM-DD.md   # 每日記錄
├── MEMORY.md           # 長期記憶（僅限主 session）
├── IDENTITY.md         # 我是誰
├── USER.md            # 關於你
├── SOUL.md            # 我的性格與原則
├── TOOLS.md           # 本地工具配置
├── HEARTBEAT.md       # 定期檢查清單
└── projects/          # 專案資料夾（建議）
```

---

### Tier 1: 個人知識庫（待建立）
**建議路徑：** `~/Documents/Knowledge/`
**用途：** 個人筆記、學習資料、參考文件
**權限：** 完全存取

**結構建議：**
```
~/Documents/Knowledge/
├── notes/              # 日常筆記
├── references/         # 參考資料、教學
├── projects/          # 專案文件
├── archives/          # 歸檔資料
└── inbox/             # 待整理（每週清空）
```

---

### Tier 2: Google Drive（待授權）
**用途：** 雲端文件、協作檔案
**權限：** 白名單資料夾

**白名單策略：**
```
Google Drive/
├── OpenClaw/          # ✅ 完全存取（專屬資料夾）
├── Work/              # ✅ 唯讀存取（需要時授權）
├── Personal/          # ❌ 未授權
└── Private/           # ❌ 永久禁止
```

---

### Tier 3: 本機其他資料夾
**用途：** 下載、桌面、專案等
**權限：** 明確指定

**白名單範例：**
- `~/Downloads/` - 唯讀（用於掃描、整理）
- `~/Desktop/` - 唯讀（避免誤刪）
- `~/Projects/` - 完全存取（開發專案）
- `~/Pictures/` - 唯讀（避免誤刪照片）

---

## 🔒 安全策略

### 禁止存取區域（黑名單）
```
❌ ~/.ssh/              # SSH 金鑰
❌ ~/.aws/              # AWS 憑證
❌ ~/.config/           # 系統配置（除非明確指定）
❌ ~/Library/Keychains/ # macOS 鑰匙圈
❌ 任何包含 "password", "secret", "private" 的檔案
```

### 敏感資料處理
- 密碼、API key → **永不記錄到 memory/**
- 財務資料 → **僅在需要時讀取，不存入長期記憶**
- 個人對話 → **摘要儲存，不記錄完整內容**

---

## 🧠 記憶管理策略

### 短期記憶（Daily Logs）
**位置：** `memory/YYYY-MM-DD.md`
**保留期限：** 30 天
**內容：**
- 每日對話摘要
- 完成的任務
- 學到的新知識
- 待辦事項

**自動清理：**
- 超過 30 天的檔案移至 `memory/archive/YYYY-MM/`

---

### 長期記憶（MEMORY.md）
**位置：** `MEMORY.md`
**用途：** 策展後的重要記憶
**內容：**
- 重要決策與原因
- 長期專案狀態
- 個人偏好與習慣
- 經驗教訓

**更新頻率：** 每週審查一次（Heartbeat 自動化）

---

### 知識索引（Knowledge Index）
**位置：** `knowledge-index.md`（待建立）
**用途：** 所有重要文件的索引
**格式：**
```markdown
## 專案

- [專案 A](~/Documents/Knowledge/projects/project-a.md) - 說明
- [專案 B](~/Documents/Knowledge/projects/project-b.md) - 說明

## 學習筆記

- [Python 進階技巧](~/Documents/Knowledge/notes/python-advanced.md)
- [OpenClaw 使用心得](workspace/projects/openclaw-notes.md)

## 重要文件

- [API 文件](https://example.com/api-docs) - 外部連結
- [配置範例](~/Documents/Knowledge/references/config-examples.md)
```

---

## 🔄 自動化管理（Heartbeat）

### 每日任務（一天 2-3 次）
- 檢查 `~/Downloads/` 是否有需要整理的檔案
- 掃描 `inbox/` 資料夾，提醒待整理內容
- 更新今日 memory log

### 每週任務（週日晚上）
- 審查過去 7 天的 daily logs
- 更新 `MEMORY.md` 與 `knowledge-index.md`
- 清理 inbox/ 資料夾
- 歸檔超過 30 天的 memory logs

### 每月任務（每月 1 日）
- 生成月度摘要報告
- 檢查 Google Drive 用量
- 審查白名單權限是否需要調整

---

## 🚀 初始化步驟

### Phase 1: 基礎設定（本週完成）
1. [ ] 建立 `~/Documents/Knowledge/` 資料夾結構
2. [ ] 建立 `knowledge-index.md`
3. [ ] 設定 Google Drive 存取（OAuth）
4. [ ] 建立 Google Drive 白名單資料夾
5. [ ] 填寫 `IDENTITY.md` 和 `USER.md`（Bootstrap 對話）

### Phase 2: 自動化（下週）
6. [ ] 配置 Heartbeat 每日檢查清單
7. [ ] 建立每週整理 cron job
8. [ ] 設定下載資料夾監控
9. [ ] 測試 Google Drive 同步

### Phase 3: 優化（持續）
10. [ ] 根據使用習慣調整分類
11. [ ] 建立常用任務的快捷指令
12. [ ] 整合其他資料源（如需要）

---

## 📊 權限總覽

| 資料夾 | 讀取 | 寫入 | 刪除 | 備註 |
|--------|------|------|------|------|
| `~/.openclaw/workspace/` | ✅ | ✅ | ✅ | 完全控制 |
| `~/Documents/Knowledge/` | ✅ | ✅ | ✅ | 知識庫 |
| `~/Downloads/` | ✅ | ❌ | ❌ | 僅整理建議 |
| `~/Desktop/` | ✅ | ❌ | ❌ | 唯讀 |
| `~/Projects/` | ✅ | ✅ | ⚠️ | 需確認後刪除 |
| Google Drive (白名單) | ✅ | ✅ | ⚠️ | 需確認後刪除 |

**圖例：**
- ✅ 完全允許
- ⚠️ 需要確認
- ❌ 禁止

---

## 💡 使用範例

### 你說：「幫我整理下載資料夾」
我會：
1. 掃描 `~/Downloads/`
2. 分類檔案（文件、圖片、安裝包等）
3. 建議移動到對應 Knowledge 資料夾
4. **不會直接刪除**，會先問你

### 你說：「記住這個專案的架構」
我會：
1. 分析專案檔案結構
2. 記錄到 `memory/YYYY-MM-DD.md`
3. 更新 `knowledge-index.md`
4. 如果重要，加入 `MEMORY.md`

### 你說：「查一下我上週寫的那篇筆記」
我會：
1. 搜尋 `memory/` 過去 7 天的檔案
2. 檢查 `knowledge-index.md`
3. 掃描 `~/Documents/Knowledge/notes/`
4. 找到後直接顯示摘要或路徑

---

**這份架構可以根據你的實際需求調整。要開始建立嗎？** 🚀
