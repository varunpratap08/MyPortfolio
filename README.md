# Varun Pratap Singh: Portfolio

A static site (plain HTML, CSS and JavaScript). No build step, no npm install.

```
portfolio/
├── index.html            page content
├── styles.css            design (light + dark theme, mobile layout)
├── script.js             theme toggle, mobile menu, resume menu, animations
└── assets/
    ├── favicon.svg
    ├── images/           your photo and screenshots go here (see below)
    │   └── og-image.png  link preview for LinkedIn / WhatsApp (already made)
    └── resume/           the two resume PDFs offered for download
```

Every image slot falls back to a designed placeholder, so the site works before you add images.
Drop a file in with the exact name below and it shows up automatically.

## Images

Already in `assets/images/`:

| File | Source |
|---|---|
| `website-builder.webp` | Screenshot of https://openkey.in |
| `calling-qr.webp` | Screenshot of https://callingqr.com |
| `cafe-cold.webp` | Admin dashboard screenshot (revenue card cropped out) |
| `quiz-home.webp`, `quiz-leaderboard.webp`, `quiz-profile.webp` | SkillBaazi app screens, status bars removed, user ID blurred |
| `gfg-academy.webp` | Admin TISP lead table; student names and dates of birth pixelated |
| `profile.jpg` | Your photo, cropped square to head and shoulders |
| `og-image.png` | Link preview image for LinkedIn / WhatsApp |

To replace an image, save the new file with the same name. If a file is missing, its slot shows a designed placeholder.
Keep each image under about 300 KB (https://squoosh.app converts PNG to WebP).

## Put it live on GitHub Pages (free)

1. On GitHub, create a new **public** repository named exactly `varunpratap08.github.io`.
2. Upload everything inside this `portfolio` folder (not the folder itself) to the repository root.
   `index.html` must sit at the top level.
3. Open the repository's **Settings → Pages**, set **Source** to "Deploy from a branch", choose `main` and `/ (root)`, and save.
4. After a minute or two the site is live at **https://varunpratap08.github.io**.

To update later, edit or upload files in that repository; the site redeploys by itself.

Netlify or Vercel also work: drag this folder onto https://app.netlify.com/drop.
If you use a different address, update the `og:url` and `og:image` lines near the top of `index.html`.

## After it's live

- **LinkedIn:** Profile → Add section → Recommended → Add featured → Add a link, and paste the URL.
  Also add it under Contact info → Website.
- **Link preview:** check how the link looks at https://www.linkedin.com/post-inspector/.
- **Resume:** set `"portfolio"` in `PROFILE` in `resume_data.py` to `varunpratap08.github.io`, then run
  `python resume_generator.py`. It will appear in the header of both resumes.
- **Resume PDFs on the site:** after rebuilding the resumes, copy the new PDFs into `assets/resume/`
  with the same file names.
