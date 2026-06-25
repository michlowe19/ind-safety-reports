# IND Safety Report Dashboard — KCI

DSMC safety report review tool for Karmanos Cancer Institute investigator-initiated trials.

## Deployment

### 1. Push to GitHub
```
git init
git add .
git commit -m "Initial deploy"
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

### 2. Connect to Netlify
1. Go to netlify.com → Add new site → Import from GitHub
2. Select this repo
3. Build settings are auto-detected from `netlify.toml`
4. Click Deploy

### 3. Add your API key
In Netlify: Site configuration → Environment variables → Add variable:
- Key: `ANTHROPIC_API_KEY`
- Value: your `sk-ant-...` key

Then trigger a redeploy (Deploys → Trigger deploy).

## Usage

1. Select a study from the dropdown — metadata pre-filled for all 6 drugs
2. Upload the tracker Excel for that study (stored in browser, only needed once)
3. Upload the ICF PDF for that study (stored in browser, only needed once)
4. Upload CTEP/CTCAE IC Terms Excel (stored once globally)
5. Drop in IND safety report PDFs → Extract & Analyze
6. Review in Report Review tab, fill in DSMC date and Local Change decisions live
7. Generate DSMC Cover Page → downloads pre-filled Word doc
8. Export session to Excel when done
