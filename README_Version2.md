# Многостраничный статический сайт (для GitHub Pages)

Это пример простого многостраничного статического сайта. Каждая страница — отдельный HTML‑файл (index.html, about.html, projects.html, contact.html, project1..project10.html) и может открываться самостоятельно.

Как опубликовать на GitHub Pages:

1. Создайте репозиторий на GitHub (например, `username/multipage-site`) или используйте репозиторий вида `username.github.io` для публикации в корне.
2. В локальной папке выполните:
   ```
   git init
   git add .
   git commit -m "Initial commit: multipage static site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```
3. На GitHub: зайдите в Settings → Pages → Source → выберите ветку `main` и папку `/ (root)`, нажмите Save.
4. Через минуту сайт будет доступен по адресу `https://<your-username>.github.io/<your-repo>/` (или `https://<your-username>.github.io/` если репозиторий называется `username.github.io`).

Локально можно тестировать через:
- Python: `python -m http.server 8000`
- или `npx http-server` (npm)

Каждая страница использует относительные ссылки и относительные пути к `assets/`, поэтому все файлы должны находиться в корне репозитория с сохранением структуры.