# Raju Gadiraju — Portfolio

Single-file portfolio website. No React, no build step, no npm. Just `index.html`.

---

## Hosting on GitHub Pages

1. Create a repo on GitHub (e.g. `prasad-portfolio`)
2. Upload `index.html` to the repo
3. Go to repo **Settings → Pages → Source → select `main` branch → Save**
4. Site is live at `https://YOUR_USERNAME.github.io/prasad-portfolio` in 1-2 minutes

---

## How to Update Content

1. Go to your repo on GitHub
2. Click `index.html`
3. Click the **pencil icon** (edit)
4. Find the section you want to change (use Ctrl+F to search)
5. Edit the text directly
6. Click **Commit changes**
7. Live site updates automatically in 1-2 minutes

---

## Where to Find Each Section

Use **Ctrl+F** in the GitHub editor to search for these markers:

| What to update | Search for |
|---|---|
| Name / contact info | `hero-contact` |
| Hero title | `hero-title` |
| Summary paragraphs | `id="summary"` |
| Skills | `id="skills"` |
| Experience (Ema, Fidelity, etc.) | `id="experience"` |
| Certifications | `id="certs"` |
| Education | `id="education"` |
| Awards | `id="awards"` |
| Contact section | `id="contact"` |

---

## Common Updates

### Change contact info

Search for `hero-contact` and edit the phone, email, LinkedIn, or location text directly.

### Update a job bullet

Search for the company name (e.g. `Ema Unlimited`). You'll see `<li class="exp-b">` tags — each one is a bullet point. Edit the text inside.

### Add a new bullet to a job

Find the job's `</ul>` tag and add a new line before it:

```html
<li class="exp-b">Your new bullet point text here.</li>
```

### Add a new skill

Search for the category name (e.g. `GPU / HPC`). You'll see `<span class="sk-tag">` tags. Add a new one:

```html
<span class="sk-tag">New Skill Name</span>
```

### Add a new certification

Search for `cert-grid`. Copy an existing `<div class="cert">...</div>` block, paste it below the last one, and change the name text.

### Add a new education entry

Search for `edu-grid`. Copy an existing `<div class="edu">...</div>` block, paste it below, and change the text.

### Update summary

Search for `id="summary"`. You'll see `<p>` tags — edit the text inside each paragraph.

### Add your photo

Replace this line:

```html
<div class="photo-initials">RG</div>
```

With:

```html
<img src="your-photo.jpg" alt="Raju Gadiraju" style="width:100%;height:100%;object-fit:cover">
```

Upload the photo to the same repo.

---

## How to Change Colors

Search for `:root{` in the file. You'll see the theme colors:

```
--bg:#060a10        → Background color
--ivory:#e8ecf4     → Main text color
--accent:#06d6a0    → Accent/highlight color (cyan-green)
--line:#141e35      → Border color
```

Change any hex color value to update the theme.

---

## Important Tips

- **Don't delete quotes or angle brackets** — the HTML will break
- **Use Ctrl+F** to find sections quickly
- **Preview before committing** — GitHub shows a Preview tab when editing
- **If something breaks** — click the file's History button on GitHub to revert to a previous version
