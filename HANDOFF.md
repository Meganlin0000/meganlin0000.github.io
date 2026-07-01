# 7aDy.bug 官網 · 完整交接與記憶檔

> 這份檔案的用途:1) 給組員看懂整個網站怎麼運作、怎麼改;2) 給接手的人（或 AI）一次掌握全部脈絡。**要改東西前先讀這份。**

---

## 1. 這是什麼

**7aDy.bug**（唸作 ladybug）＝ 淡江大學大眾傳播學系**第 41 屆畢業製作行銷組**的**招商官網**。
目的:讓**企業/廠商**看完覺得「這組專業、有創意、值得合作」，願意找我們做整合行銷、社群內容、線下活動、O2O 展演。

- 品牌概念:**Brand Debug Lab（品牌偵錯實驗室）** —— 名字是瓢蟲（ladybug）＋ Debug，「替品牌找出卡住成長的 bug，再把它修好」。
- 風格:手作企劃檔案室 × 品牌診斷報告，活潑又專業。

## 2. 網址與託管（重要）

| 用途 | 網址 |
|---|---|
| **正式網址（給廠商就給這個）** | **https://meganlin0000.github.io** |
| 備援（舊網址，也還通） | https://meganlin0000.github.io/ladybug/ |

- 託管:**GitHub Pages（免費）**，帳號 `Meganlin0000`。
- **有兩個 repo，內容一樣**:
  - `Meganlin0000/meganlin0000.github.io` → 正式根網址
  - `Meganlin0000/ladybug` → 備援
- 本機資料夾:`~/Desktop/7adybug-site/`，兩個 git remote:
  - `origin` → ladybug repo
  - `usersite` → meganlin0000.github.io repo

## 3. 團隊與聯絡

7 位成員（id 對應 `assets/team/0X.jpg`）:

| id | 姓名 | 角色 |
|--|--|--|
|01|吳苡榛|行銷企劃|
|02|陳曉恩|行銷企劃|
|03|林采頤|行銷企劃 / 財務|
|04|李汭琳|統籌|
|05|李宜臻|視覺設計|
|06|賴欣妤|社群影音 / 公關|
|07|李佩芹|社群影音 / 視覺設計|

- Email:`77ady.bug@gmail.com`　IG:`@7ady.bug_`　電話:`0908 787 823`
- ⚠️ 照片↔姓名對應是看照片配的，**請組員再核對一次有沒有配錯人**。

## 4. 檔案結構

```
7adybug-site/
├── index.html        首頁（Hero 報告拼貼 → 品牌 bug → Debug 流程 → 服務 → 案例 → 方案 → CTA）
├── about.html        團隊（故事、成員檔案卡、技能、經歷）
├── works.html        作品案例（4 張 case file + 更多作品）
├── services.html     服務與方案（6 服務 + 5 步流程 + 3 合作方向）
├── contact.html      聯絡（品牌諮詢表單）
├── member.html       單一成員頁（?id=01~07，內容由 members.js 帶入）
├── 404.html          找不到頁面（5 秒自動回首頁）
├── styles.css        全站樣式（設計系統，改配色來這）
├── script.js         互動（GSAP 捲動動畫、Lenis 平滑捲動、成員卡/表單）
├── members.js        ⭐ 七位成員的姓名/角色/介紹/專長（改文字來這）
├── site.webmanifest  App 圖示設定
├── assets/
│   ├── favicon.svg / icon-192.png / icon-512.png / apple-touch-icon.png   網站圖示
│   ├── og.png        分享到 LINE/IG/FB 會出現的預覽圖
│   ├── og.svg        （og.png 的原始檔，要改分享圖才需要）
│   └── team/01~07.jpg  七位成員照片
├── README.md         快速入門
└── HANDOFF.md        （這份）完整說明
```

## 5. 設計系統（Brand Debug Lab）

- **配色（取自履歷封面的紅黃藍）**，都定義在 `styles.css` 最上面 `:root`:
  - 奶油底 `--cream:#f7f1e6`、紙白卡 `--paper:#fffdf7`、墨黑字 `--ink:#1e1e1e`
  - **紅 `--red:#e5471e`、黃 `--yellow:#f4b41a`、藍 `--blue:#7fb2d4`**、綠 `--green:#6c8b45`
- **字體**:標題/內文 Noto Sans TC；手寫裝飾 Caveat／志莽行書；報告標籤 Space Mono。
- **手作元素**:紙張卡片（粗黑框＋位移陰影）、紅筆手繪圈選（`.circle`）、便利貼膠帶、資料夾標籤、FIXABLE 印章、Brand Bug Report 報告紙。
- **特效**:GSAP + ScrollTrigger（捲動浮現）、Lenis（平滑捲動，只在電腦）。手機首屏已改成一載入就顯示（不靠捲動）。

## 6. 怎麼改常見內容

- **改成員介紹/專長** → 開 `members.js`，每個人的 `bio`（介紹）和 `focus`（專長）直接改。
- **換成員照片** → 把新照片蓋掉 `assets/team/0X.jpg`（建議 4:5 直式）。
- **改頁面文字** → 直接開對應的 `.html` 改（結構在 HTML 裡）。
- **改配色** → `styles.css` 的 `:root` 改 `--red / --yellow / --blue` 等。
- **改方案/服務** → `services.html`（也在 `index.html` 有一份）。**價格目前刻意不公開**（寫「洽談後客製」）。

## 7. 怎麼上線更新（每次都要做）

在 `~/Desktop/7adybug-site/` 資料夾裡改完檔案後，**兩個 remote 都要 push**:

```bash
git add -A
git commit -m "更新內容"
git push origin main      # 備援 repo
git push usersite main    # 正式網址 repo
```

推完等 1~3 分鐘，GitHub Pages 會自動重新發布。**只推一個的話兩個網址會不一致。**

本機預覽(不用上線就先看):在資料夾裡跑 `python3 -m http.server 8000`，瀏覽器開 `http://localhost:8000`。

## 8. 待辦 / TODO

- [ ] **團體照**:要放在團隊頁最上面當主視覺。目前檔案還沒進資料夾——請把團體照存成 `assets/team/group.jpg`，之後接上（首頁/團隊頁預留位置）。
- [ ] 作品頁可再加**作品縮圖／IG／YouTube 連結**（目前是文字案例卡）。
- [ ] 可選加的特效:紅筆圈選「自己畫出來」、Brand Bug Report 清單「逐項打叉」（最搭偵錯概念）。
- [ ] 聯絡表單用 **formsubmit.co** 寄到 `77ady.bug@gmail.com`;**第一次有人送出時，Gmail 會收到一封啟用確認信，點一下之後才會正常收件。**

## 9. 幾個重要決定（別踩雷）

- **方案頁不放別組的案例**:履歷 PDF 的「預算方案」是用**其他組**（怪本室、七曜、HERstory…）的案子示意，**沒有放進網站**（冒用別人作品會傷信任）。網站只放 7aDy.bug 自己做過的（泰山、阿瘦、社群 16.3K、實習媒體）。
- **價格不公開**:第一眼不秀價格，改成「依需求客製、洽談後報價」，比較像顧問型團隊。
- **主軸是「抓 bug」**:整站用「找出品牌問題 → 解決」貫穿，這是跟另一組（STONE9，石頭風）最大的區隔，別稀釋掉。

## 10. 設計演進史（給接手的人 / AI）

這網站改過很多版，Megan 的偏好已經很明確，**別走回頭路**:
- v1 neubrutalism撞色 → 太像另一組、太亂 ❌
- v2 極簡編輯襯線 → 太素「不好看」❌
- v3 卡通圓角瓢蟲 → 沒質感、不喜歡卡通 ❌
- v4 白底極簡專業 → 字太大、顏色不好看 ❌
- **v5（現行）Brand Debug Lab** → 手作檔案室 + 紅黃藍活潑 ✅（照 Megan 完整指令做的）

**Megan 要的 = 手作痕跡但專業、紅黃藍活潑、每一區讓企業看得懂能解決什麼問題。不要卡通、不要科技藍紫漸層、不要滿版粉紅、不要跟 STONE9 撞。**

---

_最後更新:2026-07（v5 Brand Debug Lab，已上線根網域）_
