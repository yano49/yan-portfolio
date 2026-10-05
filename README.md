# Yan portfolio

A static site: `index.html` + `portrait.png`. No build step.

## 1. Put it on GitHub Pages
1. On GitHub create a new **public** repo, for example `yan-portfolio` (no README, no .gitignore).
2. Upload everything in this folder (including `.nojekyll`) with "Add file > Upload files", or:
   ```
   git init && git add . && git commit -m "Portfolio"
   git branch -M main
   git remote add origin https://github.com/yano49/yan-portfolio.git
   git push -u origin main
   ```
3. Repo **Settings > Pages**: Source = "Deploy from a branch", Branch = `main`, folder = `/ (root)`, Save.
4. After a minute the site is live at `https://yano49.github.io/yan-portfolio/`.

## 2. Get the domain on name.com
Use the GitHub Student Developer Pack offer (log in with GitHub on the name.com offer page), search a name (e.g. `yourname.dev`), add it to the cart and check out.

## 3. Connect the domain (name.com DNS)
In name.com: **My Domains > your domain > DNS Records**. Delete any default parking records for `@`/`www`, then add:

| Type  | Host  | Answer                |
|-------|-------|-----------------------|
| A     | (blank / @) | 185.199.108.153 |
| A     | (blank / @) | 185.199.109.153 |
| A     | (blank / @) | 185.199.110.153 |
| A     | (blank / @) | 185.199.111.153 |
| CNAME | www   | yano49.github.io      |

(These are GitHub Pages' published addresses; confirm them on GitHub's "Managing a custom domain for your GitHub Pages site" page if anything fails.)

## 4. Tell GitHub the domain
Repo **Settings > Pages > Custom domain**: type your domain (e.g. `yourname.dev`), Save, wait for the DNS check, then tick **Enforce HTTPS**.
GitHub creates a `CNAME` file in the repo for you. DNS can take from minutes to a day.

## Editing later
Open `index.html` and search for `EMAIL` (contact address), the `DATA` block (projects and events) and `ACH` (certificates). Commit the change and the site updates in about a minute.
