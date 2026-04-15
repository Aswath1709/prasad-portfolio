# Raju Gadiraju — Portfolio


- `data.js` — **all your content** (edit this to update the portfolio)
- `index.html` — the template (never needs editing)

---

## Step 1: Host on GitHub

1. Go to **github.com** → click **+** → **New repository**
2. Name it `prasad-portfolio`, keep **Public**, click **Create**
3. Click **uploading an existing file** → drag `index.html`, `data.js`, and `README.md` → click **Commit changes**

---

## Step 2: Connect Netlify (gives you a clean URL without your username)

1. Go to **netlify.com** → click **Sign up** → choose **Sign up with GitHub**
2. Already have an account? Jump to STEP 4
3. Authorize Netlify to access your GitHub account
4. Once logged in, click **Add new site** → **Import an existing project**
5. Click **GitHub** → select your `prasad-portfolio` repo
6. Leave all build settings blank (no build command, no publish directory — it's static)
7. Click **Deploy site**
8. Wait 30 seconds — your site is live with a random name like `silly-unicorn-abc123.netlify.app`
9. Go to **Site configuration** → **Change site name** → type `prasad-portfolio` → **Save**
10. Your site is now live at: **`prasad-portfolio.netlify.app`**

---

## How to Update Content

1. Go to your repo on **GitHub**
2. Click **`data.js`**
3. Click the **pencil icon** (edit)
4. Change whatever you need
5. Click **Commit changes**
6. Netlify auto-deploys in ~30 seconds — no manual deploy needed

You never need to touch `index.html`.

---

## What to Edit in data.js

| What to change | What to find in data.js |
|---|---|
| Name / phone / email | Top of file — `name`, `phone`, `email`, `linkedin` |
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

### Add a new skill
Find the category in the `skills` array and add to its `items`:
```
{ cat: "GPU / HPC", items: ["NVIDIA CUDA Toolkit", "cuBLAS", ... "YOUR NEW SKILL"] },
```

### Add a new job
Add at the **top** of the `experience` array (most recent first):
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
```
{ name: "New Cert Name", logoKey: "aws", brandColor: "#FF9900" },
```
Available logoKey values: `microsoft`, `googlecloud`, `aws`, `kubernetes`, `nvidia`, `safe`, `okta`, `cloudera`, `oracle`, `veritas`

### Add your photo
Upload the photo to the repo, then change in `data.js`:
```
photo: "photo.jpg",
```

---

## How to Change Theme Colors

This is the only thing in `index.html`. Search for `:root{` and edit:
```
--bg:#060a10        → Background
--accent:#06d6a0    → Accent color (cyan-green)
--ivory:#e8ecf4     → Text color
```

---

## Tips

- Keep quotes `"` and commas `,` intact — missing ones will break the site
- If something breaks, click **History** on GitHub to revert to a previous version
- To test locally, put both files in the same folder and open `index.html` in a browser
