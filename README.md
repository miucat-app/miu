# Miu 翻譯小貓 官方網站

Miu 翻譯小貓(LINE 群組即時翻譯機器人)的官方介紹網站,使用純 HTML/CSS/JS 製作,透過 GitHub Pages 發布。

- 線上網址(啟用 Pages 後):`https://miucat-app.github.io/miu/`
- 支援中 / 英文切換(右上角語言按鈕,記得使用者上次的選擇)
- 內容涵蓋:功能特色、支援語言、使用教學、限量試用資訊、常見問題、聯絡方式

## 檔案結構

```
miu/
├─ index.html          # 網站主頁(單頁式,所有內容都在這裡)
├─ assets/img/         # 圖片資源(吉祥物、LINE 加好友 QR code、icon、社群分享圖)
└─ .nojekyll           # 讓 GitHub Pages 直接原樣發佈檔案,不跑 Jekyll 處理
```

## 如何發布到 GitHub Pages(顯示為 你的帳號.github.io/miu/)

1. 到 GitHub 建立一個新的 **public repository**,名稱請設為 `miu`(這樣網址才會是 `.../miu/`)。
2. 在這個資料夾(`miu/`)裡執行:
   ```bash
   git remote add origin https://github.com/miucat-app/miu.git
   git branch -M main
   git push -u origin main
   ```
3. 到 GitHub 上該 repo 的 **Settings → Pages**。
4. 在 **Build and deployment → Source** 選擇 **Deploy from a branch**。
5. **Branch** 選 `main`,資料夾選 `/ (root)`,按 **Save**。
6. 等 1-2 分鐘,重新整理該頁面,會出現網址:`https://miucat-app.github.io/miu/`

之後每次要更新網站內容,只要修改 `index.html` 或圖片,`git add / commit / push` 到 `main`,GitHub Pages 就會自動重新部署。

## 之後想更新內容

- 修改文字:直接編輯 `index.html` 裡對應的中文文字,以及 `<script>` 區塊裡 `translations` 物件中對應 key 的英文翻譯。
- 換圖片:把新圖片放進 `assets/img/`,並更新 `index.html` 裡的 `<img src="...">` 路徑。
- 定價方案確定後:可以在「限量測試中」(`#trial`)與「常見問題」(`#faq`)區塊補上正式價格。
