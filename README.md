# TG 台股查詢機器人 🤖

一個基於 Telegram 的台股資訊查詢機器人，提供即時股價、K線圖表、新聞等多項功能。

## Demo (架設於免費平台，功能可能不完整)

```cmd
https://t.me/Tian_Stock_bot
```


## 🚀 快速開始

### 安裝步驟
1. Clone 專案
2. 在 `appsettings.json` 中設定您的 Telegram Bot API Key
3. 執行專案

### Docker 部署
```bash
docker build -t [your-image-name] . --no-cache
```

## 💡 功能特色

### 核心功能
- 即時股價查詢
- 技術分析圖表
- 個股新聞追蹤
- 績效資訊查看
- 多時間週期K線圖

### 採用技術
- 🤖 Telegram Bot API 整合
- 🕷️ Playwright 爬蟲技術
- ⚡ .NET 6 開發框架
- 🐳 Docker 容器化部署
- 🔄 GitHub Actions CI/CD

### 自動化部署流程
本專案採用 Git 搭配 GitHub Actions 達成自動化部署：

1. **觸發機制**
   - 為需部署的 commit 加上 tag
   - Push 至 GitHub 自動觸發部署流程

2. **CI/CD 流程**
   - **Build 階段**
     - 執行程式測試
     - 驗證功能完整性
     - 測試通過後觸發部署
   
   - **Deploy 階段**
     - 注入 Telegram Bot API Key
     - 建立並發布 Docker Image
     - 自動部署至 EC2 執行環境

## 🔧 系統架構

<img src="readme/images/flowchart.png" alt="系統架構圖" height="400" width="600">

## 📖 使用指南

### K線圖表查詢
```
/k [股票代碼] [週期]

週期選項：
h   - 時K線
d   - 日K線
w   - 週K線
m   - 月K線
5m  - 5分K線
15m - 15分K線
30m - 30分K線
60m - 60分K線
```
<img src="readme/images/kline.jpg" alt="K線示例" height="300" width="450">

### 基本資訊查詢
- 股價資訊：`/v [股票代碼]`
  
  <img src="readme/images/detail.jpg" alt="detail" height="300" width="450">
- 績效資訊：`/p [股票代碼]`
  
 <img src="readme/images/proformance.jpg" alt="proformance" height="300" width="450">
 
- 個股新聞：`/n [股票代碼]`
  
 <img src="readme/images/news.jpg" alt="news" height="300" width="450">


### TradingView 圖表
```
/chart [股票代碼]
/range [股票代碼] [時間範圍]

時間範圍選項：
1d  - 一日    5d  - 五日
1m  - 一個月  3m  - 三個月
6m  - 六個月  ytd - 今年度
1y  - 一年    5y  - 五年
all - 全部時間
```
<img src="readme/images/chart.jpg" alt="chart" height="300" width="450">

## 🔍 已知問題
- TradingView 在高頻訪問時可能會要求登入

## 📝 開發計劃
- [ ] 新增美股市場支援
- [ ] 觀察名單功能

## 🤝 貢獻指南
歡迎提交 Issue 和 Pull Request 來協助改善專案！

##  專案狀態
![Alt](https://repobeats.axiom.co/api/embed/e95b046e51a0cc699c62422b4da76c4ba6f05814.svg "Repobeats analytics image")
