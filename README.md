# ATS Tracker

A browser-based resume ATS scanner. Upload a resume (PDF, DOCX or TXT) or paste text, optionally paste a job description, and get:

- an ATS score out of 100 with a category breakdown
- knockout issues, warnings and tips, each with a fix and the points it recovers
- keyword match against the job description
- a downloadable report in PDF, Word, Markdown, HTML, plain text, JSON or CSV

Everything runs client-side. Your resume is never uploaded anywhere.

## How the score works

No ATS vendor publishes a universal score and each employer configures its own filters, so this is not the exact number a company will assign. It applies the checks systems like Workday, Greenhouse, Lever and Taleo have in common:

| Category | Points |
|---|---|
| Format and parsing | 20 |
| Contact details | 10 |
| Sections | 15 |
| Experience content | 20 |
| Keywords | 25 |
| Dates and timeline | 10 |

Knockout problems (unreadable text, missing email or phone, no experience dates, missing Experience or Education) cap the total at 64.

## Run locally

It is a single static file. Open `index.html` in a browser, or serve the folder with any static server.

## Libraries (loaded from CDN)

pdf.js, mammoth, jsPDF, JSZip.
