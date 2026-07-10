# 羽球排場系統 v2.2.0｜3x3 iPad 單機 PWA 版

這是純前端版本，不使用 Google Sheet，也不使用 Apps Script。
資料會存在使用者目前裝置與瀏覽器的 localStorage。

## 檔案

請把以下檔案上傳到 GitHub repository 根目錄：

- index.html
- manifest.webmanifest
- sw.js
- icon-192.png
- icon-512.png

## 建議 GitHub repository 名稱

badminton-3x3

## GitHub Pages 設定

1. 建立 repository：badminton-3x3
2. Upload files，上傳本資料夾全部檔案
3. 到 Settings → Pages
4. Source 選 Deploy from a branch
5. Branch 選 main，Folder 選 /root
6. Save
7. 等待 GitHub Pages 發布

網址會類似：

https://你的GitHub帳號.github.io/badminton-3x3/

## iPad 安裝方式

1. 用 iPad Safari 打開 GitHub Pages 網址
2. 點分享按鈕
3. 選「加入主畫面」
4. 名稱可改為「羽球排場」
5. 之後從主畫面圖示開啟

## 備份與還原

系統操作內有：

- 匯出備份 JSON
- 匯入備份 JSON

更新新版或換 iPad 前，請先匯出 JSON 備份。

## v2.2.0 更新

- 精簡主畫面，保留 3 個 Court 與 3 個 Next。
- Court / Next 表頭整合為下場 / 上場按鈕。
- 新增自動排場模式：下場後依場次排序補入 Next，並觸發 Next 向前遞補。
- 改善管理員工具與摺疊操作。
