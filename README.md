# Bharathwaj M — Portfolio

Plain HTML/CSS/JS, no build step or framework required.

## Structure
```
index.html      All content and page structure
css/style.css   All styling, colors, layout
js/main.js      Mobile nav toggle
```

## Adding your hero photos
The hero has a scattered polaroid-style photo gallery (3 tilted photos). Right now each
one shows a colored gradient placeholder because no image file exists yet. To add your
own photos, drop files into the `images/` folder with these exact names:
- `images/assembly-line.jpg` → the Foxconn/Korent cobot line
- `images/underwater-robot.jpg` → the TECHgium underwater inspection robot
- `images/warehouse-robot.jpg` → a mobile robot / warehouse shot

Each photo displays at roughly 230×190px and is cropped to fill (`object-fit: cover`), so
a landscape shot with the subject centered works best. If a file is missing, the gradient
placeholder shows instead of a broken image — nothing breaks.

## Editing
- **Text/content** → edit directly in `index.html` (experience, projects, skills sections are plain HTML blocks).
- **Colors** → change the CSS variables at the top of `css/style.css` under `:root`. Everything else references these, so changing one value updates the whole site.
- **Contact links** → update the `mailto:` and `href` values in the `#contact` section of `index.html`.
- **Adding a project card** → copy one `.proj-card` block in the `#projects` section and edit its text.
- **Adding a new section** (e.g. Certifications) → copy the pattern of an existing `<section>`, keep the `.seclabel` div for the heading style.

## Previewing locally
Just open `index.html` in a browser — no server needed. For live-reload while editing, you can also run:
```
npx serve .
```

## Deploying (free, ~2 minutes)
This is a static site, so any static host works:
- **Vercel**: `npx vercel` from this folder, or drag the folder into vercel.com/new
- **Netlify**: drag the folder into app.netlify.com/drop
- **GitHub Pages**: push this folder to a repo, enable Pages in repo settings

No environment variables or build config needed.
