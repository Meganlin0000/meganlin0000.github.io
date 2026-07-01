# 7aDy.bug 官方網站

淡江大傳系第 41 屆畢製**行銷組**的招商官網。純靜態網站（HTML / CSS / JS），免費架在 GitHub Pages。

### 🔗 正式網址
**https://meganlin0000.github.io**

### 📖 要改東西 / 接手前，先讀這份
👉 **[HANDOFF.md](HANDOFF.md)** —— 完整說明:網站怎麼運作、怎麼改文字/照片/配色、怎麼上線、待辦事項、重要決定與設計脈絡全都在裡面。

### ⚡ 最快上手
- **改成員介紹** → `members.js`
- **換成員照片** → `assets/team/0X.jpg`
- **改頁面文字** → 對應的 `.html`
- **改配色** → `styles.css` 最上面的 `:root`
- **本機預覽** → 資料夾裡跑 `python3 -m http.server 8000`，開 `http://localhost:8000`
- **上線** → `git add -A && git commit -m "更新" && git push origin main && git push usersite main`

### 🗂 這個資料夾裡都是網站需要的檔案
6 個頁面（index/about/works/services/contact/member）＋ 404、樣式(styles.css)、程式(script.js)、成員資料(members.js)、設定(site.webmanifest)、圖片(assets/)。**請不要刪** `assets/`、`styles.css`、`script.js`、`members.js` 或任何 `.html`，刪了網站會壞。
