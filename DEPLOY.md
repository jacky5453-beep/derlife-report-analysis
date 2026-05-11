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
- Firestore Collection：`report-whitelist`（白名單）

## 最後部署日期
2026-05-11

## 更新紀錄
- 2026-05-11：新增 ERP 損益表匯入支援（直接拉 ERP 下載的單月損益表 .xls 匯入，自動對照科目並補上缺漏科目；支援多檔批次匯入；公司／日期自動偵測）。後續預計搬到公司 NAS 內網版。
- 2026-04-15：初版部署。
