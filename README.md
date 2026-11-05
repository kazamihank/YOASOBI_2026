# 札幌 超惑星遠征手冊

三個檔案：

| 檔案 | 用途 | 要不要上傳 GitHub |
|---|---|---|
| `index.html` | **加密過的手冊**，打開只會看到密碼框，輸入密碼才解開。放到 GitHub Pages 的就是這個。 | 要 |
| `handbook.html` | 沒加密的原始手冊，自己在電腦或手機直接開。 | 不要（會被看光） |
| `build-lock.js` | 想換密碼時用：`node build-lock.js 新密碼`，會重新產生 `index.html`。 | 隨意 |

## 上 GitHub Pages

1. 在 GitHub 新建 repo，例如 `sapporo-2026`。Public 或 Private 都可以：Private 的 Pages 需要 GitHub Pro；Public 也沒關係，因為內容已加密。
2. 只上傳 `index.html`（可以順便放這個 README）。
3. repo → Settings → Pages → Source 選 `Deploy from a branch`，Branch 選 `main`、資料夾 `/ (root)`，Save。
4. 一兩分鐘後網址是 `https://kazamihank.github.io/sapporo-2026/`。
5. 手機 Safari 打開，輸入密碼，勾「在這支手機記住密碼」，之後再開就不用再輸入。加到主畫面會更像 App。

## 為什麼要加密

GitHub Pages 本身沒有「只有我能看」的設定（那是 Enterprise 才有的功能），任何知道網址的人都能開。所以手冊內容是用密碼加密後才放上去的：沒有密碼只看得到一個輸入框。密碼不會傳到任何伺服器，解密都在你的瀏覽器裡完成。

## 照片

照片直接連 Wikimedia Commons，需要網路。離線時會顯示灰底和文字，版面不會壞。

## 想改內容

改 `handbook.html`，然後重新執行 `node build-lock.js 密碼`，再把新的 `index.html` 上傳覆蓋。
