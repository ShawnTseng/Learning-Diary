# Google Drive 整合配置

## 📍 掛載位置

**Google Drive 路徑：**
```
~/Library/CloudStorage/GoogleDrive-shawntseng40@gmail.com/我的雲端硬碟/
```

**帳號：** shawntseng40@gmail.com

---

## 📁 資料夾規劃

### 本機知識庫（Knowledge）
**位置：** `~/Documents/Knowledge/`
**用途：** 本機檔案管理、快速存取
**不同步至雲端**

```
~/Documents/Knowledge/
├── inbox/          # 本機投遞區
├── notes/          # 個人筆記
├── projects/       # 專案文件
├── references/     # 參考資料
└── archives/       # 歸檔區
```

---

### Google Drive 同步區（雲端）
**位置：** `~/GoogleDrive/` → 軟連結到實際路徑
**用途：** 雲端同步、跨裝置存取、備份

**建議結構：**
```
~/GoogleDrive/
├── Sync/           # 跨裝置同步（手機、平板可存取）
├── Backup/         # 重要檔案備份
├── Archive/        # 長期歸檔
└── OpenClaw/       # 我的專用資料夾（白名單）
```

---

## 🔗 建立方便的軟連結

為了方便存取，建立桌面/主目錄捷徑：

```bash
# 主目錄捷徑
ln -s ~/Library/CloudStorage/GoogleDrive-shawntseng40@gmail.com/我的雲端硬碟 ~/GoogleDrive

# 桌面捷徑
ln -s ~/GoogleDrive ~/Desktop/GoogleDrive
```

---

## 🎯 使用策略

### 本機 Knowledge（快速、私密）
- 日常筆記、草稿
- 敏感資料（不上雲）
- 快速存取的檔案

### Google Drive（備份、同步）
- 需要跨裝置存取的檔案
- 重要文件備份
- 與他人協作的檔案

---

## 📊 權限設定

| 資料夾 | 我的權限 | 備註 |
|--------|----------|------|
| `~/Documents/Knowledge/` | 完全控制 | 本機知識庫 |
| `~/GoogleDrive/OpenClaw/` | 完全控制 | 我的專用區 |
| `~/GoogleDrive/Sync/` | 唯讀 + 建議 | 需確認後寫入 |
| `~/GoogleDrive/Backup/` | 唯讀 | 僅備份，不修改 |
| `~/GoogleDrive/Archive/` | 唯讀 | 歸檔區 |

---

## ⚠️ 注意事項

1. **暫不自動整理** - 等你指示再開始
2. **分開管理** - Knowledge 與 Google Drive 獨立運作
3. **白名單策略** - 只存取明確授權的資料夾
4. **刪除需確認** - 雲端檔案刪除前必須問你

---

**建立日期：** 2026-02-08
**更新日期：** 2026-02-08
