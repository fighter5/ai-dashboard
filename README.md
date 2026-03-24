# AI Learning Dashboard

RSS auto-fetch -> Obsidian Vault -> GitHub Pages

## Structure

```
project/
- scripts/fetch_news.py     # RSS fetcher (core)
- docs/index.html           # Preview page (deploy to GitHub Pages)
- docs/news_index.json      # Auto-generated news index
- vault/ai-news/            # Obsidian notes (auto-written .md files)
- vault/notes/              # Your personal study notes
- .github/workflows/        # Daily auto-fetch via GitHub Actions
- requirements.txt
```

## Quick Start

### 1. Install dependencies
```
pip install -r requirements.txt
```

### 2. Run fetcher
```
python scripts/fetch_news.py
```

### 3. Preview
Open docs/index.html in browser.

### 4. Use with Obsidian
Change VAULT_DIR in fetch_news.py to your vault path:
```python
VAULT_DIR = Path("/your/obsidian/vault/path/ai-news")
```

### 5. Deploy to GitHub Pages
Push to GitHub -> Settings -> Pages -> Source: main branch /docs folder

GitHub Actions will auto-run every day at 10:00 AM (UTC+8).
