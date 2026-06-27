# Percentage Calculator

Live at: https://kabeersdev.github.io/percentage_calculator/

## Files

| File | Purpose |
|------|---------|
| `index.html` | Main calculator (percentage, discount, VAT, sales tax) |
| `blog.html` | Public blog listing |
| `post.html` | Single post reader |
| `admin.html` | Private CMS dashboard |
| `data/posts.json` | All blog posts (auto-updated by admin) |
| `data/seo.json` | Global SEO settings |
| `assets/style.css` | Shared styles |

## Setup

### 1. Enable GitHub Pages
Go to repo → Settings → Pages → Source: `main` branch, `/ (root)` → Save.

### 2. Access admin
Go to `https://kabeersdev.github.io/percentage_calculator/admin.html`

On first visit, click "Set up credentials" and:
- Choose a strong password
- Paste your GitHub Personal Access Token (needs `repo` scope)
- Generate token at: https://github.com/settings/tokens/new?scopes=repo

### 3. Create posts
- Sign in to admin dashboard
- Click "New post"
- Write content with the rich text editor
- Fill in SEO fields (title, description, OG image)
- Click "Publish" — posts go live in ~30 seconds via GitHub Pages auto-deploy

## Security

- `admin.html` is password protected with SHA-256 hashed password
- Session is stored in `sessionStorage` (cleared on tab close)
- GitHub token is stored in `localStorage` (your browser only)
- Admin page has `noindex, nofollow` robots tag so search engines won't index it
- Never share your admin URL or GitHub token

## Blog CMS features

- Rich text editor (bold, italic, headings, lists, links, images)
- Per-post SEO: title, meta description, OG image, canonical URL, robots, focus keyword
- Google Search preview
- Draft / Published status
- Auto slug generation
- Global SEO settings
- Post list with edit / delete / preview
- All changes commit directly to GitHub → triggers auto-deploy
