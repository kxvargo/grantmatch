# GrantMatch — AI-Powered Grant Finder

A single-page app that uses Claude + live web search to match nonprofits with relevant grant opportunities.

## Project Structure

```
grantmatch/
├── index.html                  # Frontend
├── netlify.toml                # Netlify config
├── netlify/
│   └── functions/
│       └── claude-proxy.js     # Serverless API proxy
└── README.md
```

## Deploy to Netlify

### 1. Push to GitHub
Create a new GitHub repo and push this folder to it.

### 2. Connect to Netlify
- Go to [netlify.com](https://netlify.com) → Add new site → Import from Git
- Select your repo
- Build settings are auto-detected from `netlify.toml`
- Click **Deploy**

### 3. Add your Anthropic API Key
- In Netlify dashboard → Site → **Environment variables**
- Add: `ANTHROPIC_API_KEY` = your key from [console.anthropic.com](https://console.anthropic.com)
- Redeploy the site

### 4. Done
Your site will be live at `https://your-site-name.netlify.app`

## Local Development

```bash
npm install -g netlify-cli
netlify dev
```

Set `ANTHROPIC_API_KEY` in a `.env` file locally.
