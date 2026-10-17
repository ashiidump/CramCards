# CramCards

> **Master Your Exams with Laminated Reviewers**

CramCards is a student business project that provides affordable, subject-specific, condensed study and reviewer sets for college students. The website presents the business concept and demonstrates event-driven programming with Python in the browser through PyScript.

## Project Information

- **School:** Cebu Eastern College, Inc.
- **Department:** College of Information Technology
- **Project:** EVD — Event-Driven Programming and Business Analytics Final Project
- **Business name:** CramCards
- **Primary audience:** BSIT students
- **Initial subject focus:** Programming

## Business Concept

CramCards creates compact study materials containing topic summaries, formula sheets, key terms, flashcards, and practice prompts. Materials are designed for quick review before exams and are available as printed, digital, or bundled products.

The initial target market is BSIT students because Programming was identified as one of the most difficult subjects in the group's survey. The website presents Programming, Statistics, and Accounting reviewer sets.

## Product Pricing

| Format | Price |
| --- | ---: |
| Printed and laminated reviewer | ₱40 |
| Digital PDF reviewer | ₱30 |
| Printed + Digital Bundle | ₱50 |
| Practice sets add-on | +₱10 |

### Feasibility assumptions

- **Variable cost per set:** ₱20
- **Fixed monthly expenses:** ₱200
- **Break-even threshold:** 10 sets per month
- **Default simulator estimate:** 29 sets per month

The feasibility simulator uses this model:

```text
Revenue = Sets Sold × ₱40
Total Expenses = (Sets Sold × ₱20) + ₱200
Net Profit = Revenue − Total Expenses
```

## Survey Insights

The website displays the following research findings:

- **80.6%** of the target market are BSIT students.
- **77.4%** identified Programming as the hardest subject.
- **77.4%** prefer printed study materials.
- **67.7%** prioritize accuracy.

These figures are project survey findings rather than live market data and should be interpreted within the limitations of the student feasibility study.

## Website Features

### Business website

- Responsive CramCards landing page
- Standalone `logo.svg` brand asset used in the website header
- Deep navy, emerald, slate, and gold visual system
- Hero section with the value proposition “Master Your Exams with Laminated Reviewers”
- Promotional video-style preview
- Product showcase for Programming, Statistics, and Accounting
- Research insights dashboard with survey percentages
- Exam countdown and recommended campus pickup cutoff date

### Ordering and business tools

- Subject selector
- Printed, Digital PDF, and Bundle format options
- Practice-set add-on
- Quantity-based price calculation
- Timestamped itemized receipt
- Print or save receipt action
- Feasibility and profit-margin simulator
- Dynamic revenue, expenses, net profit, and break-even badge

### Study tools

- 25-minute Pomodoro study timer
- Start, pause, and reset controls
- Quick Programming flashcard quiz
- Reveal-answer and next-card controls

### Demo AI Study Lab

The website includes a safe **Demo AI** experience that works on GitHub Pages without an API key:

- Demo AI Study Assistant for Programming, Statistics, and Accounting
- Reviewer-style explanations for common study questions
- Demo flashcard generator for any entered topic
- Built-in study tips
- No questions are sent to an external AI service

> The current AI feature is a local demonstration, not a connection to a live AI model. A real AI integration would require a secure backend and protected API secret.

## PyScript Event-Driven Programming

Python handles the interactive behavior in the browser. The implementation is contained in the `<script type="py">` block in `index.html` and uses PyScript/Pyodide to access the DOM.

The primary event flow is:

```text
user event → Python event handler → calculation or validation → DOM update
```

Python handles:

- Order form submission and receipt generation
- Format, subject, practice-set, and quantity calculations
- Profit simulator slider updates
- Break-even status changes
- Countdown timer updates
- Product selection click events
- Pomodoro timer controls
- Flashcard quiz navigation
- Demo AI assistant responses
- Demo flashcard generation

## Technology Stack

- HTML5
- Tailwind CSS via CDN
- Font Awesome via CDN
- PyScript / Pyodide
- Python `datetime` module
- Responsive CSS
- Google Fonts via CDN
- GitHub Pages
- GitHub Actions deployment workflow

## Project Structure

```text
CramCards/
├── index.html                    # Complete single-file website and PyScript logic
├── logo.svg                      # Standalone CramCards SVG logo
├── README.md                     # Project documentation
└── .github/
    └── workflows/
        └── pages.yml             # GitHub Pages deployment workflow
```

## Run Locally

No build tools or package installation are required. The website loads PyScript and other assets from CDNs, so an internet connection is recommended.

### Clone the repository

```bash
git clone https://github.com/ashiidump/CramCards.git
cd CramCards
```

### Start a local server

```bash
python3 -m http.server 8000
```

Open the website at:

```text
http://localhost:8000
```

Opening `index.html` directly may also work, but a local server is recommended because browser security rules can affect PyScript and CDN resources when using the `file://` protocol.

## Publish with GitHub Pages

The repository includes `.github/workflows/pages.yml` for automatic deployment.

1. Upload `index.html`, `logo.svg`, and the `.github` workflow folder to the `main` branch.
2. Open the repository's **Settings → Pages** page.
3. Set the publishing source to **GitHub Actions**.
4. Open the **Actions** tab and wait for the deployment workflow to finish.
5. Visit:

```text
https://ashiidump.github.io/CramCards/
```

The `index.html` and `logo.svg` files must remain in the repository root:

```text
index.html
logo.svg
```

## Demo Walkthrough

1. Review the hero section and explain the CramCards value proposition.
2. Explore the Programming, Statistics, and Accounting product cards.
3. Select a subject and jump to the order calculator.
4. Choose a format, enable the practice-set add-on, and change the quantity.
5. Click **Calculate total** to generate the timestamped receipt.
6. Use **Print / save receipt** to open the browser print dialog.
7. Move the profit simulator slider to compare revenue, expenses, and net profit.
8. Start the Pomodoro timer and demonstrate the study sprint controls.
9. Test the flashcard quiz by revealing answers and moving to the next card.
10. Open the **Demo AI Study Lab**, ask a question, and generate topic flashcards.
11. Show the survey insights and exam countdown.

## Group Members

- Ashley Rochell B. Arcala
- Michael Probadora
- Geean Apolinar
- Adrian Estores
- Rolan Capul

## Academic Use

CramCards was created for an academic final project. Pricing, survey statistics, financial assumptions, and countdown dates are for project demonstration and educational purposes. The website does not process real orders or payments.

## License

This is an educational student project. Please contact the CramCards team before reusing its branding, business content, or materials for commercial purposes.
