# Eyes Blue Docs

這個目錄是 `eyesblue.github.io` 網站的 Git 倉庫，使用 [Just the Docs](https://just-the-docs.com/) 與 GitHub Pages 建立。

## 目前目錄規則

- 外層目錄：`C:\Users\eyesblue\Coding\AI-Coding\eyesblue.github.io`
- 網站倉庫：`C:\Users\eyesblue\Coding\AI-Coding\eyesblue.github.io\website`

使用原則：

- 不需要推上 GitHub 的說明、筆記或其他文件，放在外層 `eyesblue.github.io`
- 要發布到網站的內容，放在 `website` 目錄

## 日常操作

所有 Git 與網站相關操作都要在 `website` 目錄執行：

```powershell
cd C:\Users\eyesblue\Coding\AI-Coding\eyesblue.github.io\website
```

### 更新網站內容

```powershell
git status
git add .
git commit -m "更新網站內容"
git push
```

推送到 `main` 後，GitHub Actions 會自動重新部署網站。

## 本機預覽

已安裝 Docker Desktop 時可執行：

```powershell
cd C:\Users\eyesblue\Coding\AI-Coding\eyesblue.github.io\website
docker run --rm -it -p 4000:4000 -v "${PWD}:/srv/jekyll" -w /srv/jekyll ruby:3.3 bash -lc "bundle install && bundle exec jekyll serve --host 0.0.0.0"
```

然後開啟 `http://localhost:4000`。

## 網站位置

- GitHub Repository: `https://github.com/eyesblue/eyesblue.github.io`
- Published Site: `https://eyesblue.github.io/`
