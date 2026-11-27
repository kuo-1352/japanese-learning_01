# 日本語自學路線｜GitHub Project Pages 路徑修正版

目標網址：`https://kuo-1352.github.io/japanese-learning/`

## 本版修正重點

- 在 `index.html` 設定 `<base href="/japanese-learning/">`。
- CSS 與三個 JavaScript 檔改用 `/japanese-learning/assets/...`。
- 299 張圖片的 JavaScript 路徑改用 `/japanese-learning/assets/images/vocab/...`。
- `404.html` 的首頁連結固定回到 `/japanese-learning/`。
- 加入 `deploy-check.html`，可獨立確認 CSS、JS 與示例圖片是否已部署。
- 教材資料、30 課內容、題庫、遊戲邏輯與 299 張圖片都未刪減。

## 必須這樣重新上傳

1. 解壓縮 ZIP。
2. 在 repository 根目錄刪除或覆蓋舊版檔案。
3. 上傳解壓後的**內容本身**，不要把外層資料夾或 ZIP 當成一個檔案上傳。
4. Repository 根目錄必須直接看到：

```text
index.html
404.html
deploy-check.html
README.md
assets/
```

5. `assets` 下必須保留：

```text
assets/css/style.css
assets/js/images.js
assets/js/lessons.js
assets/js/app.js
assets/images/vocab/L01_01.jpg ...
```

6. 等 GitHub Pages deployment 變成 Active 後，先開：
   `https://kuo-1352.github.io/japanese-learning/deploy-check.html`
7. 五項都出現綠色 `✓` 後，再開首頁。
8. 若仍看到舊的無樣式畫面，使用無痕視窗，或在網址後暫加 `?v=2`。
