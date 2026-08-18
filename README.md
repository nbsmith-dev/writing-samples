# Nathan B. Smith — Technical Writing Samples

**Live site: [nbsmith-dev.github.io/writing-samples](https://nbsmith-dev.github.io/writing-samples/)**

A self-contained portfolio of technical writing samples across seven skill
areas — secure network systems, API documentation, curriculum development and
systems engineering, structured authoring, standards compliance, editing
craft, and systems/process thinking. The site is a single static HTML page
served from GitHub Pages: no build step, no framework, nothing to keep
patched.

All samples are hypothetical, non-proprietary demonstration works built
around fictional systems and a fictional owning company (TechCoaches
Information Systems Design). Nothing here contains classified,
export-controlled, or proprietary data; every part number, drawing, and
technical value is invented, and each deliverable carries its own disclaimer.

## Repository layout

```
.
├── index.html                  ← the portfolio page (also hosts the analytics snippet)
├── Nathan_Smith_Resume.pdf     ← resume, linked from the page header
├── samples/                    ← every deliverable, prefixed by sample ID
├── .gitignore
└── README.md
```

## Sample inventory

Files in `samples/` are prefixed with the ID shown on the card
(`SAMPLE-nn`). A sample may ship as several files — an HTML companion for
reading in-browser, a PDF for download, and a `.zip` of DITA source or SVG
diagrams. Section numbers below match the section numbers on the page.

### 01 — Secure Network Systems (SNS)

| ID | Sample | Files |
| --- | --- | --- |
| 14 | System Security and Privacy Plan — ECN-100 Expeditionary Command Node (DoD RMF, NIST SP 800-53, CNSSI 1253; DDIL operations) | `14-ecn100-sspp.html`, `14-ecn100-sspp.pdf`, `14-ecn100-diagrams-svg.zip` |
| 26 | System Security Plan — VSG-100 Secure Network Gateway (NIST SP 800-171 / DFARS 252.204-7012, CMMC, DITA) | `26-vsg100-ssp-nist800171.html`, `26-vsg100-ssp-nist800171.pdf`, `26-vsg100-diagrams-svg.zip` |
| 27 | VSG-100 Installation Guide (DITA task/reference, hazard-statement discipline, panel drawings) | `27-vsg100-installation-guide.html`, `27-vsg100-installation-guide.pdf`, `27-vsg100-diagrams-svg.zip` |

### 02 — API Documentation

| ID | Sample | Files |
| --- | --- | --- |
| 28 | Vehicle Management API — TC-77 Skylark (REST, mTLS, DITA-authored, published as a docs-site page) | `28-tc77-vms-api-guide.html`, `28-tc77-vms-api-guide-dita-source.zip` |

### 03 — Featured Proposal

| ID | Sample | Files |
| --- | --- | --- |
| 00 | From Governance Framework to Practice — white paper adapting the dissertation's LLM governance framework to a specific role | `00-white-paper-collins-aerospace.pdf` |

### 04 — Structured Authoring

| ID | Sample | Files |
| --- | --- | --- |
| 02 | Fault Isolation Procedure — High Vibration Alarm (S1000D, decision-tree logic) | `02-fault-isolation-procedure.pdf` |
| 03 | Illustrated Parts Catalog — Turbine Air Inlet Assembly (S1000D Issue 5.0, BOM/CAGE) | `03-s1000d-ipc-excerpt.pdf` |
| 04 | Systems Operator Guide — Startup, Operation & Shutdown | `04-systems-operator-guide.pdf` |
| 05 | Lube Oil Filter Element — Removal and Installation (S1000D Issue 4.2, ATA 72-60) | `05-s1000d-removal-installation.pdf` |
| 07 | AI-Assisted Work Instruction — ISO 9001 / AS9100D (DITA 1.3 topic set + map) | `07-dita-iso-work-instruction-preview.pdf`, `07-dita-iso-work-instruction-source.zip` |

### 05 — Standards Compliance

| ID | Sample | Files |
| --- | --- | --- |
| 11 | The Authority Stack — Which Standard Wins (seven-tier precedence model, DI-IPSC, CUI/RMF) | `11-documentation-standards-stack.pdf` |

### 06 — Editing Craft

| ID | Sample | Files |
| --- | --- | --- |
| 01 | Simplified Technical English: Before & After (ASD-STE100) | `01-ste-editing-before-after.pdf` |
| 08 | Legacy Procedure Remediation — Hydraulic Test Stand HTS-100 (defect index, rewrite, rationale) | `08-legacy-procedure-remediation-hts100.pdf` |
| 09 | Passive to Active — one-page editing reference (interactive HTML) | `09-passive-to-active-cheat-sheet.html` |
| 10 | ASD-STE100 — Ten Rules That Fix Most of It (interactive HTML with live checker) | `10-ste100-cheat-sheet.html` |

### 07 — Systems & Process Thinking

| ID | Sample | Files |
| --- | --- | --- |
| 06 | AI-Assisted Technical Documentation: A Governance Workflow | `06-ai-governance-workflow.pdf` |
| 12 | Documentation Change Control and Delivery Tracking Procedure (DITA, GitLab workflow, CUI marking) | `12-documentation-change-control-procedure.pdf` |
| 13 | C++ for Technical Writers (from-zero tutorial) | `13-cpp-for-technical-writers.pdf` |

### 08 — Curriculum Development & Systems Engineering

A single NAVEDTRA M-142 document chain for one course, *Linux
Administration from the Command Line*, built for operators of the ECN-100
platform documented in SAMPLE-14. Each document consumes the outputs of the
ones before it; open items (CCA assignment, lab-environment sourcing) are
carried forward deliberately.

| ID | Sample | File |
| --- | --- | --- |
| 15 | Alignment Brief | `15-alignment-brief-linux-cli-ecn100.pdf` |
| 25 | Resource Sponsor Funding Notification (naval letter format) | `25-funding-notification-ecn100.pdf` |
| 16 | Front End Analysis (FEA) Report | `16-fea-report-linux-cli-ecn100.pdf` |
| 17 | Curriculum Outline of Instruction (COI) | `17-coi-linux-cli-ecn100.pdf` |
| 18 | Instructional Performance Requirements Document (IPRD v2) | `18-iprd-v2-linux-cli-ecn100.pdf` |
| 19 | Instructional Media Requirements Document (IMRD) | `19-imrd-linux-cli-ecn100.pdf` |
| 20 | Draft Training Course Control Document (TCCD) | `20-draft-tccd-linux-cli-ecn100.pdf` |
| 21 | Draft Course Master Schedule (CMS) | `21-draft-cms-linux-cli-ecn100.pdf` |
| 22 | Draft Resource Requirements List (RRL) | `22-draft-rrl-linux-cli-ecn100.pdf` |
| 23 | Instructional Media Design Package (IMDP) | `23-imdp-linux-cli-ecn100.pdf` |
| 24 | Instructor / Facilitator Guide (Draft) | `24-instructor-guide-linux-cli-ecn100.pdf` |

SAMPLE-25 is numbered after the rest but sits second in the chain, between
the Alignment Brief and the FEA, because that's where it falls
chronologically in the process.

## Maintaining the site

**Replacing a sample.** Drop the new file in `samples/` under the same
filename and nothing else changes. If you rename it, update every matching
`href` in `index.html` — most cards carry two or three buttons pointing at
the same or related files.

**Adding a sample.** Assign the next ID, name the file `nn-short-slug.ext`,
add it to `samples/`, then copy an existing `<article class="card">` block
into the right section and edit the DMC line, title, tags, description, and
all button links.

**Verify links before pushing.** Card markup is added by hand, so a filename
typo or a file that never got uploaded produces a silent 404 on a live page:

```bash
grep -o 'samples/[^"]*' index.html | sort -u > /tmp/referenced.txt
ls samples/ | sed 's|^|samples/|' | sort > /tmp/present.txt
comm -23 /tmp/referenced.txt /tmp/present.txt   # linked but missing
comm -13 /tmp/referenced.txt /tmp/present.txt   # present but orphaned
```

**Filename rules that matter.** No spaces, no parentheses. Pages serves each
file at its literal path, so a space becomes `%20` in the URL and a stray
`(1)` from a re-upload silently creates an orphaned second copy.

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
  only, which is enough to tell whether a link sent to a recruiter got
  opened.
- **Issue number.** The page header carries a document control line
  (`DOC-NBS-PORTFOLIO-001 · Issue n · date`). Bump it whenever samples are
  added or removed, the same way any controlled document would be.
- **HTML companions.** Several samples ship as both a self-contained HTML
  page and a PDF. The HTML is wired to the card's primary View button, since
  it opens in-browser on a phone without a download.
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
