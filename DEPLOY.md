# 報表分析系統 — 部署資訊

## 部署平台
GitHub Pages

## GitHub Repo
https://github.com/jacky5453-beep/derlife-report-analysis

## 線上網址
https://jacky5453-beep.github.io/derlife-report-analysis/

## 部署指令
```bash
cd "/Users/jacky/Desktop/claude/claude code/報表分析系統"
git add -A && git commit -m "描述" && git push origin main
# GitHub Pages 自動部署
```

## 環境變數
無（Firebase config 內嵌於 HTML）

## Firebase 設定
- 專案：derlife-audit
- Authentication：Google 登入
- Firestore Collections：
  - `report-whitelist`（白名單，role: admin/user）
  - `report-data/main`（全公司共用資料，白名單成員可讀寫；資料用 JSON 字串存於 `dataJson` 欄位，含兩家公司的 pl + baseData）

## 權限說明
- **管理員 (admin)**：完整功能 + 可管理白名單（新增／移除帳號）
- **使用者 (user)**：可讀資料、可匯入 ERP、可編輯（給財務人員用此角色）
- 不論 admin/user，看到的都是同一份 `report-data/main` 共用資料

## 最後部署日期
2026-05-11

## 更新紀錄
- 2026-05-11（晚）：加入 Firestore 雲端同步＋共用資料機制。匯入／編輯／刪除年度都會自動同步到 Firestore，重新整理或換裝置都不再掉資料。白名單內所有成員（含財務人員）看到的是同一份資料。
- 2026-05-11（早）：新增 ERP 損益表匯入支援（直接拉 ERP 下載的單月損益表 .xls 匯入，自動對照科目並補上缺漏科目；支援多檔批次匯入；公司／日期自動偵測）。後續預計搬到公司 NAS 內網版。
- 2026-04-15：初版部署。
