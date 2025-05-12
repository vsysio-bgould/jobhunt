# THE FANTASTIC JOB FINDER 2000

*"I never said I was great at naming things." -Some guy, probably*

## What is this?

This repository contains a set of YAML files designed to optimize my job search.
These YAML files can be pasted into a conversation with an LLM, such as ChatGPT,
and they will be faithfully executed.

## Prerequisites

* ChatGPT (or other LLM) account, preferably "Plus" or even "Pro." The free tier is
  probably insufficient for the amount of work we'll be throwing at it.
* Keyboard.
* Monitor.
* Heartbeat.
* Patience.

## Find Jobs (Job Finder.yaml)

This document instructs GPT to locate job postings that may be a fit for your
achievements and experience.

### Features

* Finds jobs based on the information you wrote into the YAML file.
* Searches job boards (LinkedIn, Indeed, etc.) but also searches corporate websites
  for jobs that aren't on job boards yet. It also considers other avenues--one time,
  it sent me a job posted to Reddit. Another time, it sent me a link to a Crypto
  forum post. Very cool.
* Flags jobs that are a particularly strong fit, and will explain why it believes so.
* Queries sites like Glassdoor and other sources to identify interesting findings that
  could be red or green flags for an applicant. For example, it will flag reports of 
  layoffs, poor morale and high turnover. Conversely, if it finds good reports, it
  will post those findings as well.
* Assesses companies for high turnover, and will try to speculate as to the cause.
* Applies a disqualifying bias for persons who have strong experience in one Cloud 
  platform but not another (AWS, Azure, etc.). It will not consider, for instance,
  "AWS EC2" to be a transferable skill for "Azure Virtual Machines" as those are two
  distinct services.
* Highlights jobs that were recently posted less than 4 hours ago--before they've been
  flooded with 7,698 applicants.
* Disqualifies jobs where more than a configurable number have already applied.
* Constrains results not to geographic area but to work authorization eligibility. 
  For example, in my case, it's much easier for me to work remotely for a company in
  the British Commonwealth than the United States.
* Does not discriminate based on job title--it's not uncommon for a class of work to 
  carry many titles. DevOps is an example of this; I have seen DevOps jobs entitled as
  Systems Analyst, Release Coordinator, Magical Wizard, Server Operator, etc.
* A paging mechanism intended to let it optimize its own resources. A search this large
  is likely to exceed context windows, causing hallucinations (it started listing
  mortician  jobs for me once--har har), and so it will only process a handful of jobs
  at a time.  When ready for the next batch, say "Next"
* Exports resulting findings as CSV or XLSX.

### Quick Tips

**Be as detailed as possible** in describing your background

Don't mention experience with a Cloud provider (AWS, Azure etc.) **unless you have
  strong experience with it**--leverage its disqualifying bias to find you the best fitting roles.

**Feel free to add sections to widen your search.** For example, if you published a book, you could include:

```yaml
Authoring: # Books I've written
  - Name: "The Greatest Book Ever Written"
    ISBN: "182920-3-299292"
    Description: "Jeremy is an IT engineer who ..."
    Topics:
      - DevOps
      - IT
      - AWS
     ( ... )
      - Web Servers
```

**You can hint as to the purpose of a section using a comment.** See preceding authorship example.

### Quickstart

1. Copy the included sample YAML files and modify them to suit your circumstances.
2. Open a conversation with ChatGPT.
3. Ensure the model selected is "o3" or better.
4. Paste the entire YAML file into a code fence (ie. 3 backticks followed by yaml,
   the yaml itself, and then 3 backticks to close the block)
5. Wait a while - it takes up to 10 minutes usually.
6. It will produce a list of job postings that it believes you're a good fit for.
7. Optionally download the generated CSV or Excel sheet.
8. When ready for the next batch, say "Next".

## Build Resume (Resume Builder.yaml)

NOTE: Section under construction.

