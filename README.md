# Raju Gadiraju — Portfolio


- `data.js` — **all your content** (edit this to update the portfolio)
- `index.html` — the template (never needs editing)

---

## Hosting on GitHub Pages

1. Create a repo on GitHub (e.g. `prasad-portfolio`)
2. Upload both `index.html` and `data.js`
3. Go to repo **Settings → Pages → Source → select `main` branch → Save**
4. Live in 1-2 minutes

---

## How to Update Content

1. Go to your repo on GitHub
2. Click **`data.js`**
3. Click the **pencil icon** (edit)
4. Change whatever you need
5. Click **Commit changes**
6. Live site at https://USERNAME.github.io/REPO-NAME updates in 1-2 minutes

You never need to touch `index.html`.

---

## What to Edit in data.js

| What to change | What to find in data.js |
|---|---|
| Name / phone / email | Top of the file — `name`, `phone`, `email`, `linkedin` |
| Hero title | `heroTitle` |
| Summary | `summaryP1`, `summaryP2`, `summaryP3` |
| Stats (years, certs, etc.) | `stats` array |
| Available-for tags | `availableFor` array |
| Skills | `skills` array — each has `cat` (category name) and `items` (list) |
| Job experience | `experience` array — each has `company`, `role`, `dates`, `bullets` |
| Certifications | `certifications` array |
| Education | `education` array |
| Awards | `awards` array |
| Photo | Change `photo: null` to `photo: "photo.jpg"` and upload the image to the repo |

---

## Examples

### Add a new skill to an existing category
Find the category in the `skills` array and add to its `items`:
```
{ cat: "GPU / HPC", items: ["NVIDIA CUDA Toolkit", "cuBLAS", ... "YOUR NEW SKILL"] },
```

### Add a new job
Add a new entry at the **top** of the `experience` array (most recent first):
```
{
  company: "New Company",
  role: "Your Title",
  location: "City, State",
  dates: "Jan 2026 – Present",
  bullets: [
    "First responsibility.",
    "Second responsibility.",
  ],
},
```

### Add a new certification
Add to the `certifications` array:
```
{ name: "New Cert Name", logoKey: "aws", brandColor: "#FF9900" },
```
Available logoKey values: `microsoft`, `googlecloud`, `aws`, `kubernetes`, `nvidia`, `safe`, `okta`, `cloudera`, `oracle`, `veritas`

### Update summary
Just edit the text inside `summaryP1`, `summaryP2`, or `summaryP3`.

---

## How to Change Theme Colors

Edit the `:root` section inside `index.html`:
```
--bg:#060a10        → Background
--accent:#06d6a0    → Accent color (cyan-green)
--ivory:#e8ecf4     → Text color
```

---

## Tips

- Keep quotes `"` and commas `,` intact — missing ones will break the site
- If something breaks, use GitHub's **History** button to revert
- Test locally by opening `index.html` in a browser (both files must be in the same folder)
