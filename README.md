# Yonatan Mitiku — Architectural Portfolio

A static portfolio site (plain HTML, CSS and JavaScript, no build step).

## Structure

```
index.html      the whole site (project data is the PROJECTS array near the bottom)
images/<slug>/  NN.jpg (full size) and NN-t.jpg (thumbnail) for each project
video/          project walkthrough videos and poster images
```

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Push to GitHub

```bash
git init
git add .
git commit -m "Add portfolio site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## Deploy

**Vercel:** import the GitHub repo at vercel.com/new. Leave Framework Preset as "Other" and leave the build command and output directory empty.

**GitHub Pages:** repo Settings > Pages > Deploy from a branch > `main` / root. The site appears at `https://<your-username>.github.io/<repo-name>/`.

**Netlify:** import the repo, leave the build command empty, publish directory `.`.

## Edit or add a project

1. Add photos to `images/<slug>/` named `01.jpg`, `02.jpg`, ... with matching `01-t.jpg` thumbnails (about 800 px wide).
2. Add an entry to the `PROJECTS` array in `index.html`: `R('<slug>', <number of photos>)` lists the photos. Add `video` and `poster` for a video.

## Contact details

Phone, email and the Telegram link are in the `#contact` section of `index.html`. The contact form has no server: on submit it opens the visitor's email app with the message filled in, addressed to the email in the form script. To receive messages directly in the page without an email app, connect the form to a form service such as Formspree or Netlify Forms.
