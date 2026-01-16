# TWT Site Audit
>A fast, local, and extensible CLI tool for SEO and website quality audits.

![Python](https://img.shields.io/badge/Python-3.11+-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![CLI Tool](https://img.shields.io/badge/Type-CLI-orange)

TWT Site Audit is a lightweight command-line SEO and website quality scanner built for small businesses, developers, and consultants who need fast, actionable insights without bloated enterprise tools.

It fetches a webpage, analyzes core SEO and structural signals, and generates a clear audit report you can use for diagnostics, proposals, or ongoing monitoring.

---

## Why TWT Site Audit Exists

Most site audits are:
- Overkill for small sites
- Locked behind paid dashboards
- Slow to run or hard to automate

TWT Site Audit focuses on clarity, speed, and ownership:
- Run it locally
- Understand the results immediately
- Extend it however you want

This project was built as a production-quality MVP and is suitable for real client work.

---

## Core Features

- Command-line interface (CLI)
- Fetches and parses live HTML
- SEO and quality checks
- Structured data models for results
- JSON report output
- Clean, extensible architecture

---

## Checks Performed

Current checks include:

- Page title presence and content
- Meta description presence and length
- H1 and H2 heading extraction
- Image `alt` attribute validation
- Canonical link detection
- Basic page structure analysis

Designed so new checks can be added in minutes.

---

## Tech Stack

- Python 3.11+
- Requests
- BeautifulSoup4
- lxml
- Rich (console formatting)
- Dataclasses
- Argparse

---

## Project Structure
'''text
twt-site-audit/
│
├── twt_site_audit/
│ ├── init.py
│ ├── main.py
│ ├── cli.py
│ ├── fetch.py
│ ├── parse.py
│ ├── checks.py
│ └── report.py
│
├── outputs/ # Generated reports (gitignored)
├── .gitignore
├── README.md
├── requirements.txt
└── LICENSE
'''
---

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/techwiththisguy/twt-site-audit.git
cd twt-site-audit
```

### 2. Create and activate a virtual environment (Windows)
```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Usage
```bash
python -m twt_site_audit https://example.com
```

### Optional flags
```bash
--max-pages 10
```

## Output

- Console summary (human-readable)
- Structured JSON report saved to the `outputs/` directory

Example output file:
```
outputs/audit_example.com_YYYYMMDD-HHMMSS.json
```

This makes it easy to:
- Share results with clients
- Feed data into other tools
- Track improvements over time

## Example Use Cases

- SEO diagnostics for client proposals  
- Pre-launch site quality checks  
- Developer QA workflows  
- Lightweight alternative to heavy audit platforms  
- Foundation for automated monitoring  

## Roadmap

Planned enhancements:
- Internal link crawling
- Broken link detection
- Core Web Vitals placeholders
- CSV export
- GitHub Actions automation
- Plugin-style check registration

## Development Philosophy

This project prioritizes:
- Readability over cleverness
- Extensibility over abstraction
- Ownership over dependency lock-in

## License

MIT License — free to use, modify, and distribute.

## Author

Built by **Tech With Thisguy LLC**  
Software Development • Web • Automation
