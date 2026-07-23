# 羽球排場系統 v2.4.6｜2x2 / 3x3 iPhone 17 Pro 主要版

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

## iPhone 安裝方式

1. 用 iPhone Safari 打開 GitHub Pages 網址
2. 點分享按鈕
3. 選「加入主畫面」
4. 名稱可改為「羽球排場」
5. 之後從主畫面圖示開啟

## 舊 iPad Air 診斷頁

如果舊 iPad Air 無法顯示主畫面，先開啟：

https://ksp4022-ko.github.io/badminton-3x3/ipad-test.html?v=1

診斷頁會檢查 Safari / Web App 模式、Service Worker、Cache、icon、manifest、主版版本、JS 語法、viewport、Storage、觸控與語音支援。

## 球員名單備份與還原

系統操作內有：

- 匯出球員名單 JSON
- 匯入球員名單 JSON

備份保存球員姓名、已打場次、貼紙顏色、新增順序與群組資料。匯入後所有球員會回到休息區，不保存 Court / Next 位置，也不切換目前 2x2 / 3x3 模式。

## v2.2.0 更新

- 精簡主畫面，保留 3 個 Court 與 3 個 Next。
- Court / Next 表頭整合為下場 / 上場按鈕。
- 新增自動排場模式：下場後依場次排序補入 Next，並觸發 Next 向前遞補。
- 改善管理員工具與摺疊操作。

## v2.2.1 更新

- 選取提示改為上方浮層，不再推動 Court / Next 版面。
- 新增球員時可用 12 色色塊選擇貼紙底色。
- 隨機填滿場地改為依序補滿 Court 1-3，再補 Next 1-3。
- 置換 PWA icon，已由 1024 來源圖產生 512 與 192 圖示。

## v2.3.0 更新

- 管理員工具新增 2x2 / 3x3 模式切換，切換前必須先清空 Court / Next。
- 2x2 模式只顯示 Court 1-2 與 Next 1-2，隨機填滿與自動排場會跟隨目前模式。
- 匯出 / 匯入改為球員名單備份，不再保存場上或等待區位置。
- 新增球員貼紙顏色選中狀態改為外框、勾勾與微放大。
- 折疊區塊改用右側箭頭顯示展開 / 收合，球員管理也支援折疊。

## v2.3.1 更新

- Court / Next / 休息區球員選取狀態改為內框、勾勾與陰影，避免被格子裁切。
- 休息區與 Admin 改為一致的折疊區塊，並記住折疊狀態。
- Admin 已登入時標題顯示「Admin 已登入」，登入後保持展開。
- 自動呼叫改為 Admin 內的折疊子功能，語音設定不再二層折疊。
- Admin 內只顯示自動呼叫、球員管理、場次管理、系統操作四項子功能。

## v2.3.2 更新

- 自動排場改為先讓 Next 1 上場並向前遞補，再把下場人員排入 Next 空格。
- 自動呼叫語音加入目標場地，例如「A、B、C、D 請上一號場」。
- 隨機填滿場地不再觸發自動呼叫，也不覆蓋最後呼叫名單。
- 場次管理按鈕配色依操作風險統一。
- 取消選取按鈕改為高反差，重複點同一球員可取消選取。
- 新資料預設使用自動排場，舊資料保留既有設定。

## v2.3.3 更新

- 移除主版舊 Safari 不支援的 optional chaining 與 nullish coalescing 語法。
- 補上 `vh` fallback，保留 `dvh` 給新裝置使用。
- 浮動按鈕拖曳新增 touch / mouse fallback，支援沒有 PointerEvent 的舊 iPad。
- 更新 Service Worker cache，協助舊裝置取得新版。

## v2.4.0 更新

- 新增 Admin 群組管理，可建立群組、加入選取球員、移除選取球員與刪除群組。
- 自動排場時，同群組下場球員優先排入相同 Next；空格不足時仍允許拆開並排滿可用空格。
- 若同群組成員已在某個 Next，新的同群組下場球員會優先補進該 Next。
- 手動搬移優先，不會自動復原或重排既有 Next。
- 球員名單備份新增群組資料，匯入後仍全部回休息區。

## v2.4.1 更新

- 浮動管理工具恢復 v2.3.2 的 pointer/click 穩定事件流程。
- 移除 v2.3.3 為舊 iPad 加入的 touch / mouse fallback，避免 iPhone PWA 點擊被攔截。
- 恢復現代 Safari 語法與 iPhone 17 Pro 主要版 CSS 寫法。

## v2.4.2 更新

- 修正群組管理「加入選取球員」為選取操作警示配色。
- 修正「今日重新開始」為全域重置危險配色。
- 已選取 Court / Next 球員後，再點另一位 Court / Next 球員可直接交換位置。
- 涉及休息區球員時不交換，改為選取新點擊球員，避免誤觸上場。

## v2.4.3 更新

- 加入選取球員成功後會釋放選取狀態。
- 移除選取球員群組成功後會釋放選取狀態。
- 無效操作仍保留選取狀態，方便繼續建立群組或修正操作。
## v2.4.4 更新

- Court 表頭改為顯示「⬇ 下場」，讓下場操作更明確。
- Next 表頭保留人數顯示。
- Next 上場到 Court 後，目標 Court 會顯示 4 秒「上場」高亮特效。
## v2.4.5 更新

- 自動呼叫新增自訂播報模板，支援 `{players}`、`{court}`。
- 播報模板空白時維持原本預設格式。
- 整體網頁背景改為深綠灰，讓上場 Court 高亮更明顯。
## v2.4.6 更新

- 整體配色改為深碳黑背景、亮藍 Court、中灰 Next、綠色上場特效。
- 上場中的 Court 卡片加入淡綠底色，提升層次與辨識度。
- Court / Next 表頭加入立體按鈕效果。
- 上場提示改為 `請上場` 半形點點動畫。
