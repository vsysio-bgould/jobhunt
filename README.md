# Fantastic Job Finder 2000
*"I never said I was great at naming things." — someone, probably*

> **YAML‑powered job‑search workflows for ChatGPT & other LLMs**

## Table of Contents
1. [Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Job‑Finder Workflow](#job-finder-workflow)  
   &nbsp;&nbsp;• [Key Features](#key-features)  
   &nbsp;&nbsp;• [Quick Tips](#quick-tips)  
   &nbsp;&nbsp;• [Quick‑Start](#quick-start)
4. [Resume Builder](#resume-builder)
5. [License](#license)

---

## Overview
This repo ships **drop‑in YAML playbooks** that steer an LLM (e.g., ChatGPT) through every phase of a technical job search—finding openings, flagging red/green signals, and prepping application materials.  
Paste a YAML file into ChatGPT and watch the model work.

---

## Prerequisites
| Requirement | Notes |
|-------------|-------|
| ChatGPT Plus/Pro (or comparable LLM) | Free tier may throttle long searches |
| Keyboard & display | You know the drill |
| Heartbeat & patience | Large searches can take a few minutes |

---

## Job‑Finder Workflow (`Job Finder.yaml`) <a id="job-finder-workflow"></a>

### Key Features <a id="key-features"></a>
- **Multi‑source search** — LinkedIn, Indeed, company sites, Reddit, niche forums, and more.
- **Fit scoring** — Flags standout roles and explains the rationale.
- **Company due diligence** — Surfaces Glassdoor reviews, layoff news, morale cues, etc.
- **Turnover insights** — Highlights churn and speculates on root causes.
- **Strict skill matching** — Treats AWS ≠ Azure ≠ GCP (no fuzzy “cloud” equivalence).
- **Early‑bird alerts** — Marks postings < 4 h old—beat the applicant deluge.
- **Applicant‑count filter** — Skips roles already flooded with candidates.
- **Work‑authorization filter** — Focuses on where you can *legally* work, not *where* you live. Finds remote roles out-of-country.
- **Title agnostic** — Detects relevant roles no matter how quirky the title.
- **Paging** — Stays within context limits; reply **Next** for more results.
- **Export** — One‑click CSV/XLSX download.

### Quick Tips <a id="quick-tips"></a>

- **Be specific.** The more detail you pack into your YAML, the sharper the matches.
- **List only clouds you truly know.** A strict AWS ≠ Azure ≠ GCP bias weeds out mismatches in your favor.
- **Extend the schema** for books, patents, open‑source work—whatever sells your story:

  ~~~yaml
  # Example: Author credits
  Authoring:
    - Name: "The Greatest Book Ever Written"
      ISBN: "182920-3-299292"
      Description: "Jeremy is an IT engineer who ..."
      Topics: [DevOps, AWS, Web Servers]
  ~~~

  <sup>*Tip:* Inline comments (`# like this`) help the LLM interpret custom sections.</sup>

### Quick‑Start <a id="quick-start"></a>
1. Copy `Job Finder.yaml` (or start with the sample) and edit your details.
2. Open ChatGPT and select **o3** or better.
3. Paste the YAML inside a fenced block:
   ~~~yaml
   # your YAML here
   ~~~
4. Wait—runs can take up to **10 minutes**.
5. Review suggested postings; download CSV/XLSX if desired.
6. Type **Next** for the next page.

---

## Resume Builder (`Resume Builder.yaml`) <a id="resume-builder"></a>
*Coming soon — generate ATS‑friendly, tailored resumes in seconds.*

---

## License <a id="license"></a>
MIT — see [LICENSE](LICENSE) for details.
