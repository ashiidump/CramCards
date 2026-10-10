# CramCards — Verified Review Sets

> **Subject-specific reviewer sets for college students**
>
> A Business Analytics and Event-Driven Programming final project by Cebu Eastern College students.

## Project Overview

CramCards is a student-made reviewer-set business that creates compact, subject-specific study materials for college students. Each set combines topic summaries, key-term or formula sheets, flashcards, and practice prompts in a format designed for the final days before an exam.

The first product line focuses on **BSIT Programming subjects**, where students often need a fast and reliable way to review concepts such as variables, loops, functions, arrays, and logic. Sets are available as printed, digital, or printed-plus-digital bundles and are prepared for campus pickup after order confirmation.

The website demonstrates how a business concept can be presented through a functional website while applying **PyScript** and **event-driven programming**.

## Group Members

| Member | Suggested contribution area |
| --- | --- |
| Arcala, Ashley Rochell B. | Business concept, research, and content |
| Probadora, Michael | PyScript interactions and order customizer |
| Apolinar, Geean | Website layout, responsive styling, and visual design |
| Estores, Adrian | Feasibility-study data, evidence section, and calculator |
| Capul, Rolan | Testing, documentation, presentation, and GitHub organization |

> Update the contribution areas to reflect the work each member actually completed. Every member should make meaningful commits to this repository.

## Business Concept

| Item | CramCards decision |
| --- | --- |
| Business type | Printed, laminated, and digital study/review materials |
| Initial target market | College students, beginning with BSIT students |
| First subject focus | Programming Foundations |
| Base selling price | ₱40 per set |
| Estimated variable cost | ₱20 per set |
| Main differentiator | Student-made and accuracy-checked content designed for a specific course |
| Order pathway | Website estimate, Messenger or Google Form confirmation, campus pickup |

The feasibility study found that **96.8%** of respondents were open to the idea by answering “Yes” or “Maybe,” **77.4%** wanted printed materials in some form, and **67.7%** considered accuracy and completeness their most important purchasing factor. The initial survey included 31 college students and was concentrated among BSIT respondents, so the business begins as a small Programming pilot.

## Website Features

### Business website

- Hero section that explains the problem CramCards solves.
- Product catalog for Programming, Statistics, and custom subject requests.
- Pricing and format information based on the feasibility study.
- Ordering process from set selection to campus pickup.
- Evidence section with survey findings and limitations.
- Responsive layout for desktop and mobile screens.

### PyScript and event-driven programming

- Catalog button click events move a selected subject into the order customizer.
- Format changes update the visual selection and price estimate.
- Quantity input, plus, and minus events recalculate the order total.
- Form submission is intercepted by a Python handler, validated, and displayed in a confirmation dialog.
- The study-time calculator reads user input, performs a calculation, and updates the page without reloading.

The central pattern is:

```text
user event → Python event handler → calculation or validation → DOM update
```

## Project Structure

```text
.
├── index.html                 # Main website content and page sections
├── styles.css                 # Responsive design system and visual styling
├── main.py                    # PyScript event handlers and DOM updates
├── pyscript.toml              # PyScript runtime configuration
├── manus-routes.json          # Root route manifest for static preview/publishing
├── public/
│   └── manus-routes.json      # Webdev route-manifest copy
├── cramcards-logo.svg         # Brand mark
├── app.config.ts              # Project logo metadata
├── TODO.md                    # Project outcome checklist
├── COMMIT_GUIDE.md            # Group Git workflow and commit guide
└── README.md                  # This documentation
```

## Run the Website Locally

The website is static and can be served with Python's built-in HTTP server:

```bash
python3 -m http.server 3000 --bind 0.0.0.0
```

Open `http://localhost:3000` in a browser.

The website loads PyScript and Google Fonts from CDNs, so an internet connection is needed for the complete experience. If Python is unavailable, use another static server such as VS Code Live Server.

## How to Demonstrate the Website

1. Introduce CramCards, the target customers, and the verified-accuracy value proposition.
2. Scroll through the product catalog and explain why Programming is the first product line.
3. Click **Choose this set** to move a product into the order customizer.
4. Change the format and quantity to show the live price calculation.
5. Submit the order demo and explain the validation and confirmation dialog.
6. Enter different values into the study-time calculator and show the dynamic result.
7. Show the feasibility-study evidence and explain the market limitation.
8. Open `main.py` and trace an event from `addEventListener` to the Python handler and DOM update.
9. Have each member explain their actual contribution and meaningful commits.

## Data and Business Assumptions

The content is based on the group's feasibility study, not on live sales data. The main assumptions are:

- ₱40 selling price per set.
- ₱20 estimated variable cost per set.
- A reachable initial market of approximately 150 students.
- Demand concentrated around exam periods.
- Campus pickup and direct social-media ordering rather than online payment.

The feasibility decision is **feasible with conditions**: begin with a small Programming pilot, verify every set for accuracy, keep costs near ₱20 per set, and measure actual sales before expanding to other subjects.

## Academic Project Information

- **Course:** FREE ELEC 1 – Business Analytics
- **Project:** From Data to Business: A Mini Feasibility Study and Functional Business Website
- **School:** Cebu Eastern College, Inc. — College of Information Technology
- **Section/Schedule:** FS 6:00–7:30 PM / Section 4
- **Instructor:** Mr. Vincent John Cababan
- **Date:** September 29, 2026

## Repository and Contribution Policy

This repository should be public before submission. Each member must contribute meaningful work under their own GitHub account. Being listed as a collaborator is not enough: the instructor may review the commit history and changed files.

Read [COMMIT_GUIDE.md](COMMIT_GUIDE.md) before making changes.

## License and Academic Use

This project was created for academic purposes. The CramCards business concept, branding, content, and code belong to the student group unless otherwise noted.
