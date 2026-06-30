# Team Portal

A corporate landing page powered by [Decap CMS](https://decapcms.org/) and hosted on [Netlify](https://netlify.com).

## Features

- ✅ Public landing page with rich text, images, links and file downloads
- ✅ Browser-based CMS editor at `/admin` — no code needed to update content
- ✅ Invite-only editor access (2 editors)
- ✅ All content and uploads stored in this Git repository

## Project Structure

```
team-portal/
├── admin/
│   ├── index.html          # CMS editor UI
│   └── config.yml          # CMS field definitions
├── content/
│   └── page.md             # Page content (front matter + markdown body)
├── uploads/                # Images and file attachments (managed by CMS)
├── index.html              # Public landing page
└── netlify.toml            # Netlify build and header config
```

## Setup Instructions

### 1. Update `admin/config.yml`

Replace the placeholder in `config.yml` with your GitHub username:

```yaml
backend:
  name: github
  repo: GeekJenAI/team-portal
```

### 2. Push to GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/team-portal.git
git push -u origin main
```

### 3. Deploy on Netlify

1. Go to [app.netlify.com](https://app.netlify.com) → **Add new site → Import an existing project**
2. Connect to GitHub and select this repo
3. Build command: *(leave blank)*
4. Publish directory: `.`
5. Click **Deploy site**

### 4. Enable Identity & Git Gateway

1. Netlify dashboard → **Site configuration → Identity → Enable Identity**
2. Set registration to **Invite only**
3. Scroll to **Services → Git Gateway → Enable Git Gateway**
4. **Identity → Invite users** → invite both editors by email

### 5. Edit Content

Navigate to `https://your-site.netlify.app/admin` and log in with your invited email.

## Editing Content

The CMS at `/admin` lets you:

| Field | What it does |
|---|---|
| **Page Title** | Main heading shown in the header |
| **Subtitle** | Subtext shown below the title |
| **Hero Image** | Full-width banner image |
| **Body Content** | Rich text (markdown) — headings, bold, lists, links, code |
| **Links** | List of labelled redirect links shown on the page |
| **File Attachments** | Uploadable files that visitors can download |

## License

Internal use only.
