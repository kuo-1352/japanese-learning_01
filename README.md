# 日本語自學路線｜GitHub Pages 修正版

這個資料夾已把原本約 11 MB 的單一 HTML 拆成 GitHub Pages 適用的靜態網站。

## 結構

```text
japanese-learning/
├── index.html
├── 404.html
├── .nojekyll
├── README.md
└── assets/
    ├── css/style.css
    ├── js/images.js
    ├── js/lessons.js
    ├── js/app.js
    └── images/vocab/   # 299 張單字圖片 + manifest.json
```

## 上傳方式（GitHub 網頁版）

1. 解壓縮 ZIP。
2. 進入 GitHub repository `japanese-learning`。
3. 建議先刪除舊的單一 `index.html`，再選 **Add file → Upload files**。
4. 把「解壓後資料夾內的所有內容」上傳到 repository 根目錄；不要只上傳 ZIP。
5. 確認 repository 首頁直接看到 `index.html` 與 `assets` 資料夾。
6. 到 **Settings → Pages**，選擇：
   - Source: Deploy from a branch
   - Branch: main
   - Folder: / (root)
7. 儲存並等待 deployment 變成綠色 Active，再開啟：
   `https://kuo-1352.github.io/japanese-learning/`

## 這版修正

- 將 299 張 Base64 圖片抽成實際 JPEG/PNG，避免瀏覽器先解析 11 MB 內嵌 JavaScript。
- CSS、課程資料、圖片索引與應用程式分檔載入。
- 所有資源使用 `./assets/...` 相對路徑，支援 GitHub Project Pages 子路徑。
- 學習進度資料損壞時會安全重設，不再造成整頁停止初始化。
- 載入失敗時會顯示可讀錯誤訊息，而不是只呈現白頁。
- 保留 15 Day、30 Lesson、299 張圖片詞卡、文法、情境、測驗、遊戲與本機進度。

## 本機快速測試

不要直接雙擊 `index.html`；在此資料夾執行：

```bash
python -m http.server 8000
```

再開啟 `http://localhost:8000/`。
