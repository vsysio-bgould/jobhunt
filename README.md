# Fantastic Job Finder 2000
*"I never said I was great at naming things." — someone, probably*

> **YAML‑powered job‑search workflows for ChatGPT & other LLMs**

## Table of Contents
1. [Overview](#overview)
2. [Message to Employers](#message-to-employers)
3. [Prerequisites](#prerequisites)
4. [Job‑Finder Workflow](#job-finder-workflow)  
   &nbsp;&nbsp;• [Key Features](#key-features)  
   &nbsp;&nbsp;• [Quick Tips](#quick-tips)  
   &nbsp;&nbsp;• [Quick‑Start](#quick-start)
5. [Resume Builder](#resume-builder)
6. [License](#license)

---

## Overview
This repo ships **drop‑in YAML playbooks** that steer an LLM (e.g., ChatGPT) through every phase of a technical job search—finding openings, flagging red/green signals, and prepping application materials.  
Paste a YAML file into ChatGPT and watch the model work.

---

## Message to Employers <a id="message-to-employers"></a>

Hiring managers and HR partners often ask why a candidate would let an AI system help
shape their résumé. Here’s the thinking behind my approach.

### Why I enlist AI

- **Role-specific focus.** Every job ad uses its own mix of keywords and priorities.
  Instead of sending you the same static résumé I give everyone else, I let an AI
  reorganize my work history so the achievements most relevant to *your* posting rise
  to the top. **You spend less time hunting for the details that matter.**
- **Speed with purpose.** Classic advice tells candidates to rewrite a résumé for every
  application; that can eat up hours per role. Off-loading the mechanical cutting,
  pasting, and re-ordering to a language model frees those hours for higher-value
  activities, such as studying the latest AWS releases, completing certification renewals, and
  contributing code to open-source projects you can inspect. In short, the time saved
  shows up as stronger skills when I join your team.

### How I keep the facts straight

1. **Single source of truth.** All titles, dates, certifications, project metrics, and
   public links live in one structured file inside this repository.
2. **Prompt safeguards.** The AI is instructed to *re-format* or *re-phrase* what’s in
   that file—**but never to invent new facts.** This keeps the résumé honest and
   accurate.
3. **Human verification.** I personally read and sign off on every résumé before it is
   submitted.
4. **Full audit trail.** Because the data and prompts are version-controlled, you can
   always ask to see exactly what produced the résumé on your desk.

### What this means for you

- **Clearer screening.** The résumé you receive surfaces the skills, tools, and results
  you listed in the job description, reducing guesswork in the first pass.
- **Transparency by design.** Curious about any line item? I can point you to the
  project repo, architecture diagram, or reference that backs it up.
- **Continuous improvement.** The same AI-powered workflow that trims paperwork on my
  end lets me reinvest energy into staying current with industry trends—*benefiting the
  teams I join.*
- **Working demonstration of my skills.** The résumé you receive is a working example
  of my ability to *think* outside the box, *automate* repetitive tasks and *augment* my own capabilities using
  language models. It’s a great way to prove my candidacy beyond tools and technologies.

*If you’d like to review the underlying data or discuss how a particular accomplishment
might translate to your environment, just let me know. I’m happy to walk through the
details.*

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

## Resume Builder (`Resume Builder.yaml`) <a id="resume-builder"></a>

### Key Features <a id="key-features-resume"></a>
- **ATS-aware layout** — Generates résumés that parse cleanly in Workday, Greenhouse, Lever, iCIMS, and other major applicant-tracking systems.
- **Role-tailored emphasis** — Pulls the bullets, metrics, and keywords from your YAML that most closely match *this* job description—no more generic “kitchen-sink” résumé.
- **Metric spotlighting** — Automatically surfaces quantifiable wins (e.g., “reduced AWS spend 32 %,” “cut deployment time 80 %”) to catch a screener’s eye.
- **One- or two-page control** — Dial the length up or down without hand-editing.
- **Template presets** — Choose Chronological, Hybrid, or Functional templates—each color-safe and printer-friendly.
- **Version tracking** — Every résumé variant is stored as a diff in Git so you can roll back or audit changes.
- **Guardrails against fabrication** — Uses only the facts in your YAML; see “Message to Employers” for the anti-hallucination rules.
- **Export** — One-click download as PDF, Markdown, or DOCX (experimental).

### Quick Tips <a id="quick-tips-resume"></a>
- **Feed it numbers.** Recruiters love metrics; include cost savings, uptime gains, and delivery speed improvements in your YAML.
- **Rank your skills.** An ordered list lets the builder decide what to keep when space is tight.
- **Tag industries.** Label experience by domain (FinTech, MedTech, GovCloud) so the builder can echo the hiring company’s sector.
- **Use inline comments.** `# like this` — they help the model interpret any custom fields you add.
- **Audit generated resumes.** The builder is a helpful starting point, but it’s not perfect. Always review the output and make tweaks as needed.

### Quick-Start <a id="quick-start-resume"></a>
1. Copy `Resume Builder.yaml` (or start with the sample) and fill in your canonical data.
2. Open ChatGPT (o3 or better).
3. Paste the YAML inside a fenced block:
   ~~~yaml
   # your Resume Builder YAML here
   ~~~  
4. Wait until it confirms that it understands what you want it to do.
5. Paste the job description. Raw text dump is usually OK--no need to clean it up, unless it's a horrible mess.
6. Wait **30–60 seconds** for the formatted résumé preview.
7. Provide special instructions to, for example, emphasize one priority fact about you.
8. Ask for a **Cover letter** if you want it to generate a cover letter.

---

## License <a id="license"></a>
MIT — see [LICENSE](LICENSE) for details.
