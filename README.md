# 紀念日計算器網站

這是使用 [Just the Docs](https://just-the-docs.com/) 與 GitHub Pages 建立的獨立網站。

## 首次發布

1. 在 GitHub 建立一個空白 repository（不要勾選 README、`.gitignore` 或 License）。
2. 在此目錄執行：

   ```powershell
   git remote add origin https://github.com/<你的帳號>/<repository名稱>.git
   git push -u origin main
   ```

3. 打開 repository 的 `Settings` → `Pages`。
4. 在 `Build and deployment` 的 `Source` 選擇 `GitHub Actions`。
5. 打開 `Actions`，確認 `Deploy Jekyll site to Pages` 成功。若第一次執行發生在 Pages 啟用之前而失敗，請按 `Re-run all jobs`。

網站網址通常是 `https://<你的帳號>.github.io/<repository名稱>/`。若 repository 名稱是 `<你的帳號>.github.io`，網址則是 `https://<你的帳號>.github.io/`。

## 本機預覽

已安裝 Docker Desktop 時可執行：

```powershell
docker run --rm -it -p 4000:4000 -v "${PWD}:/srv/jekyll" -w /srv/jekyll ruby:3.3 bash -lc "bundle install && bundle exec jekyll serve --host 0.0.0.0"
```

然後開啟 `http://localhost:4000`。
