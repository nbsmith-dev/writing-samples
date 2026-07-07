# Nathan B. Smith — Technical Writing Samples

A small, self-contained portfolio site showcasing S1000D / MIL-STD technical
writing samples (IETMs, fault isolation procedures, illustrated parts
catalogs, operator guides, and STE editing work). Built as a single static
HTML page so it can be hosted for free on GitHub Pages — no build step
required.

## What's in this repo

```
.
├── index.html                  ← the portfolio page
├── Nathan_Smith_Resume.pdf     ← resume, linked from the page header
├── samples/
│   ├── 01-ste-editing-before-after.pdf
│   ├── 02-fault-isolation-procedure.pdf
│   ├── 03-s1000d-ipc-excerpt.pdf
│   ├── 04-systems-operator-guide.pdf
│   └── 05-s1000d-removal-installation.pdf
└── README.md
```

All samples are hypothetical, non-proprietary demonstration works — each PDF
carries its own disclaimer on the cover page.

## Publish it on GitHub Pages (one-time setup, ~5 minutes)

1. **Create a new repository on GitHub.**
   Go to [github.com/new](https://github.com/new), name it something like
   `writing-samples` (the URL will be
   `https://github.com/<your-username>/writing-samples`), leave it **public**
   (Pages needs a public repo unless you have GitHub Pro/Enterprise), and
   don't initialize it with a README (you already have one).

2. **Push this folder to the new repo.** From inside this folder, run:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio: technical writing samples"
   git branch -M main
   git remote add origin https://github.com/<your-username>/writing-samples.git
   git push -u origin main
   ```

3. **Turn on GitHub Pages.**
   In the repo on GitHub: **Settings → Pages** (left sidebar, under "Code and
   automation"). Under **Build and deployment → Source**, choose
   **Deploy from a branch**. Under **Branch**, choose `main` and folder
   `/ (root)`, then click **Save**.

4. **Wait ~1 minute, then visit your live site.**
   GitHub will show the URL at the top of that same Pages settings screen —
   it will look like:
   ```
   https://<your-username>.github.io/writing-samples/
   ```
   That's the link to send hiring managers. They can read each sample
   (View PDF) or save it locally (Download) directly from the page.

## Updating a sample later

Replace the file in `samples/` (keep the same filename, or update the link
in `index.html` if you rename it), then:
```bash
git add .
git commit -m "Update sample"
git push
```
GitHub Pages redeploys automatically within a minute or two.

## Notes

- The page is plain HTML/CSS with no external dependencies besides Google
  Fonts (IBM Plex Sans/Mono), so it loads fast and has no maintenance
  overhead.
- If you'd rather use a custom domain (e.g. `portfolio.nathansmith.dev`),
  add a `CNAME` file to the repo root containing just the domain, and point
  a DNS `CNAME` record at `<your-username>.github.io` — GitHub's Pages docs
  walk through this under **Settings → Pages → Custom domain**.
