# Nathan B. Smith — Technical Writing Samples

**Live site: [nbsmith-dev.github.io/writing-samples](https://nbsmith-dev.github.io/writing-samples/)**

A self-contained portfolio of technical writing samples spanning S1000D and
MIL-STD aviation maintenance data, DITA-authored security and installation
documentation, ISO work instructions, curriculum development, and API
documentation. The site is a single static HTML page served from GitHub
Pages — no build step, no framework, nothing to keep patched.

All samples are hypothetical, non-proprietary demonstration works built
around fictional systems and a fictional owning company (TechCoaches
Information Systems Design). Each deliverable carries its own disclaimer:
no export-controlled, CUI, or classified information is contained in these
documents.

## Repository layout

```
.
├── index.html                  ← the portfolio page (also hosts the analytics snippet)
├── Nathan_Smith_Resume.pdf     ← resume, linked from the page header
├── samples/                    ← every deliverable, numbered by sample ID
├── .gitignore
└── README.md
```

## Sample inventory

Files in `samples/` are prefixed with the sample ID used on the page
(`SAMPLE-nn`). A sample may ship as more than one file — an HTML companion
for reading in-browser, a PDF for download, and a `.zip` of source or
diagram assets.

### STE and legacy content remediation

| ID | Files | What it demonstrates |
| --- | --- | --- |
| 01 | `01-ste-editing-before-after.pdf` | Source prose rewritten to ASD-STE100 — controlled vocabulary, one instruction per sentence, ambiguity removed. |
| 08 | `08-legacy-procedure-remediation-hts100.pdf` | An inherited legacy procedure (HTS-100) rebuilt into a usable, standards-conformant maintenance task. |
| 09 | `09-passive-to-active-cheat-sheet.html` | Quick-reference card for converting passive constructions to active voice. |
| 10 | `10-ste100-cheat-sheet.html` | Quick-reference card for the ASD-STE100 rules that come up most in practice. |

### S1000D / MIL-STD aviation maintenance data

| ID | Files | What it demonstrates |
| --- | --- | --- |
| 02 | `02-fault-isolation-procedure.pdf` | Diagnostic logic written as a decision path a technician can follow at the aircraft. |
| 03 | `03-s1000d-ipc-excerpt.pdf` | Illustrated parts data structured to the S1000D schema, with figure/item callout correspondence. |
| 04 | `04-systems-operator-guide.pdf` | Task-oriented operator documentation — what the system does, how to run it, what the indications mean. |
| 05 | `05-s1000d-removal-installation.pdf` | A maintenance data module: preliminary requirements, procedure steps, and close-out requirements in schema-valid form. |

### Secure Network Systems (SNS)

| ID | Files | What it demonstrates |
| --- | --- | --- |
| 14 | `14-ecn100-sspp.html`, `14-ecn100-sspp.pdf` | ECN-100 Expeditionary Command Node System Security and Privacy Plan — DoD RMF format (NIST SP 800-53, CNSSI 1253, DoDI 8510.01) authored in DITA, covering DDIL operations, EMCON, and COMSEC key management. |
| 26 | `26-vsg100-ssp-nist800171.html`, `26-vsg100-ssp-nist800171.pdf`, `26-vsg100-diagrams-svg.zip` | VSG-100 Secure Network Gateway System Security Plan mapped to NIST SP 800-171, plus the hand-authored SVG diagram set (architecture, data flow, rack elevation, sequence, swimlane, key lifecycle, panel drawings). |
| 27 | `27-vsg100-installation-guide.html`, `27-vsg100-installation-guide.pdf`, `27-vsg100-diagrams-svg.zip` | DITA-authored hardware installation guide — site requirements, five installation tasks, and front/rear panel reference topics with distinct Note/Caution/Warning treatments. |

### API documentation

| ID | Files | What it demonstrates |
| --- | --- | --- |
| 28 | `28-tc77-vms-api-guide.html`, `28-tc77-vms-api-guide-dita-source.zip` | TC-77 Skylark vehicle management system API guide — concept, task, and reference topics authored in DITA, with the DITA source included so the structure is inspectable. |

### Process, standards, and governance

| ID | Files | What it demonstrates |
| --- | --- | --- |
| 00 | `00-white-paper-collins-aerospace.pdf` | Long-form technical white paper written for an aerospace audience. |
| 06 | `06-ai-governance-workflow.pdf` | A documented workflow for governing AI use inside a documentation pipeline. |
| 07 | `07-dita-iso-work-instruction-preview.pdf`, `07-dita-iso-work-instruction-source.zip` | ISO-style work instruction authored in DITA, with source included. |
| 11 | `11-documentation-standards-stack.pdf` | How the standards layer together in practice — S1000D, DITA, STE, ISO — and where each one actually applies. |
| 12 | `12-documentation-change-control-procedure.pdf` | A change control procedure for a documentation set: who approves what, and how revisions are tracked. |
| 13 | `13-cpp-for-technical-writers.pdf` | C++ concepts explained for writers who have to document code they didn't write. |

## Maintaining the site

**Replacing a sample.** Drop the new file in `samples/` under the same
filename and nothing else has to change. If you rename it, update the
matching `href` in `index.html`.

**Adding a sample.** Assign the next sample ID, name the file
`nn-short-slug.ext`, add it to `samples/`, then copy an existing card block
in `index.html` and edit the title, category, description, and every button
link on the card. Cards commonly carry two or three buttons (View HTML /
Download PDF / Download source or diagrams) — check that each one resolves.

**Filename rules that matter.** No spaces and no parentheses. GitHub Pages
serves the file at its literal path, so a space becomes `%20` in the URL and
a stray `(1)` from a re-upload silently creates a second, orphaned copy.

Then:

```bash
git add .
git commit -m "Update sample"
git push
```

GitHub Pages redeploys automatically within a minute or two. If a change
doesn't appear, hard-refresh — browsers cache PDFs aggressively.

## Notes

- **No external dependencies** beyond Google Fonts (IBM Plex Sans/Mono), so
  the page loads fast and carries effectively zero maintenance overhead.
- **Cloudflare Web Analytics** is embedded in `index.html`. It's cookie-free
  and doesn't fingerprint visitors — it reports page views and referrers
  only, which is enough to tell whether a link sent to a recruiter actually
  got opened.
- **HTML companions.** Several samples ship as both a self-contained HTML
  page and a PDF. The HTML version is the one wired to the card's primary
  View button, since it opens in-browser on a phone without a download.
- **Custom domain.** To serve this from something like
  `portfolio.nathansmith.dev`, add a `CNAME` file to the repo root
  containing just the domain, then point a DNS `CNAME` record at
  `nbsmith-dev.github.io`. Configure it under **Settings → Pages → Custom
  domain** and enable **Enforce HTTPS** once the certificate provisions.

<details>
<summary><strong>First-time setup (already done for this repo — kept for reference)</strong></summary>

1. **Create the repository.** At [github.com/new](https://github.com/new),
   name it `writing-samples`, leave it **public** (Pages requires a public
   repo unless you have GitHub Pro or Enterprise), and skip README
   initialization.

2. **Push the folder.**

   ```bash
   git init
   git add .
   git commit -m "Initial portfolio: technical writing samples"
   git branch -M main
   git remote add origin https://github.com/<your-username>/writing-samples.git
   git push -u origin main
   ```

3. **Enable Pages.** **Settings → Pages → Build and deployment**. Set
   **Source** to *Deploy from a branch*, **Branch** to `main`, folder
   `/ (root)`, and save.

4. **Wait about a minute.** The live URL appears at the top of the same
   Pages settings screen, in the form
   `https://<your-username>.github.io/writing-samples/`.

</details>
