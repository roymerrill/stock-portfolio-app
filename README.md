# Stock Portfolio — Public Site

This repo hosts the public-facing website for **Stock Portfolio** (the Mac + iOS app).
The app's source code lives in a separate private repository.

## Setup steps

1. Create a new **public** GitHub repo named `stock-portfolio-app`
   (or any name — just update the URLs in `index.html`)

2. Push this folder's contents to that repo:
   ```bash
   cd ~/Desktop/StockPortfolioSite
   git init
   git add .
   git commit -m "Initial site"
   git remote add origin https://github.com/roymerrill/stock-portfolio-app.git
   git push -u origin main
   ```

3. Enable GitHub Pages:
   - Repo Settings → Pages → Source: **Deploy from branch** → `main` / `/ (root)`
   - Your site will be live at: `https://roymerrill.github.io/stock-portfolio-app/`

4. Copy the App Store screenshots:
   ```bash
   mkdir -p screenshots
   cp ~/Desktop/AppStoreScreenshots/01_portfolio_dashboard.png screenshots/
   cp ~/Desktop/AppStoreScreenshots/02_lot_detail.png screenshots/
   cp ~/Desktop/AppStoreScreenshots/03_settings.png screenshots/
   git add screenshots/
   git commit -m "Add screenshots"
   git push
   ```

5. Upload the Mac DMG as a GitHub Release:
   - Go to: Releases → Draft a new release
   - Tag: `v0.1.0`
   - Title: `Stock Portfolio 0.1.0`
   - Attach: `StockPortfolio.dmg`
   - The download button in `index.html` already links to:
     `https://github.com/roymerrill/stock-portfolio-app/releases/latest/download/StockPortfolio.dmg`

6. Update the App Store link in `index.html` once the app is live:
   Replace `idYOUR_APP_ID` with your actual App Store app ID.
