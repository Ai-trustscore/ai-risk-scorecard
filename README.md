# AI Risk Scorecard

這是一個單頁互動式 AI 風險評估工具，使用 15 個問題分析 5 個 AI 風險領域。

## 已優化項目

- 改用語義化按鈕和可訪問的 `aria-live` 區塊
- 改善進度條與結果動畫
- 精簡樣式並維持響應式佈局
- 增加 Open Graph metadata 以提升分享效果

## 發佈方式

### GitHub Pages
1. 將 `index.html` 和 `README.md` 加入版本控制。
2. 推送到 GitHub。
3. 在 repository 設定中啟用 GitHub Pages，選擇 `main` 分支的根目錄。
4. 你的網站將於 `https://<your-username>.github.io/<repo-name>/` 可用。

### Netlify / Vercel
1. 建立新的專案。
2. 上傳此資料夾或連結到 GitHub repository。
3. 部署後即可取得公開網址。

### 本地預覽
- 直接打開 `index.html`。
- 或使用簡單伺服器：
  ```bash
  python3 -m http.server 8000
  ```
  然後開啟 `http://localhost:8000`。

### 自動部署 (GitHub Actions)

此專案已包含一個 GitHub Actions workflow，會在推送到 `main` 分支時自動部署站點到 GitHub Pages：

- Workflow 檔案： `.github/workflows/deploy-pages.yml`

步驟（範例）:

1. 在本機建立倉庫或將本專案加入 git：

```bash
cd /path/to/ai-risk-scorecard
git init
git add .
git commit -m "Initial commit: AI Risk Scorecard"
git branch -M main
git remote add origin git@github.com:<your-username>/<repo-name>.git
git push -u origin main
```

2. 推送後，GitHub Actions 會自動運行並將站點部署到 GitHub Pages（需要 repository 的 `Pages` 權限允許 Actions 寫入）。

3. 若要自訂網域，請在 repository 設定的 Pages 區域設定自訂網域，或在 repository 根目錄新增 `CNAME` 檔案。

故障排除：
- 若頁面未顯示，檢查 Actions 執行紀錄（Actions -> workflow -> Deploy to GitHub Pages）。
- 確認 repository 的 `Settings -> Pages` 設定允許使用 GitHub Actions 做為發佈來源。

