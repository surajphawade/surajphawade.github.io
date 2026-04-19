# Suraj Phawade — Portfolio Website

A modern, interactive personal portfolio website built for GitHub Pages deployment.

## 🚀 Deploy to GitHub Pages

### Option 1: Replace your existing site
```bash
# 1. Clone your existing repo
git clone https://github.com/surajphawade/surajphawade.github.io
cd surajphawade.github.io

# 2. Copy the new index.html
cp /path/to/downloaded/index.html .

# 3. Commit and push
git add index.html
git commit -m "feat: new portfolio site with admin panel & blog"
git push origin main
```

Your site will be live at: **https://surajphawade.github.io**

### Option 2: Fresh deploy
```bash
git init
git add index.html README.md
git commit -m "initial portfolio"
git branch -M main
git remote add origin https://github.com/surajphawade/surajphawade.github.io.git
git push -u origin main
```

---

## 🔐 Admin Panel

To manage your portfolio content from the browser:

1. Click the **⚙ Admin** link in the top-right of the navbar
2. Enter the password: `suraj2024`
3. You can now:
   - Add/delete **Skill** categories
   - Add/delete **Experience** entries
   - Add/delete **Certifications**
   - Write and publish **Blog posts**

> **Important:** To change the admin password, open `index.html` and find:
> ```javascript
> const ADMIN_PASS = 'suraj2024';
> ```
> Change `suraj2024` to your desired password and re-deploy.

### 📦 How data is stored
All dynamic content (skills, experience, certifications, blog posts) is saved in **localStorage** in the visitor's browser. This means:
- Your edits persist across page refreshes on the same browser/device
- To keep content permanent across all visitors, you have two options:
  1. **Edit the defaults in the HTML file** — find `DEFAULT_SKILLS`, `DEFAULT_EXPERIENCE`, `DEFAULT_CERTS` in the `<script>` section and update them manually, then redeploy
  2. **Use a backend** (future upgrade: GitHub Gist, Firebase, Supabase)

---

## ✍️ Writing Blog Posts

1. Login to Admin Panel
2. Click the **Blog** tab
3. Fill in: Title, Category Tag, Excerpt, Full Content, and an Emoji icon
4. Click **Publish Post**
5. The post instantly appears in the Blog section

---

## 🎨 Customization

| What to change | Where in `index.html` |
|---|---|
| Admin password | `const ADMIN_PASS = 'suraj2024'` |
| Your name & title | Hero section HTML |
| Contact email | `handleContactForm()` function & contact section |
| LinkedIn / GitHub URLs | Contact section `<a>` tags |
| Color scheme | `:root` CSS variables at top |
| Default resume data | `DEFAULT_SKILLS`, `DEFAULT_EXPERIENCE`, `DEFAULT_CERTS` arrays |

---

## 🛠 Tech Stack
- Pure HTML/CSS/JavaScript — no frameworks, no build tools
- Google Fonts (Syne + DM Sans + JetBrains Mono)
- localStorage for dynamic content
- Intersection Observer API for scroll animations
- GitHub Pages for hosting

---

Built with ❤ · Suraj Phawade · Pune, India
