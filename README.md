# QAOpsPlaywright

**A hands-on learning project by a Test Manager learning modern automation — from the governance side in.**

> *"A QA leader who understands what automation can and can't do is more valuable than one who only manages spreadsheets. This repo is how I'm building that understanding."*

---

## Why this repo exists

I've spent 17 years in quality governance — defining test strategies, managing 20+ QA teams, and overseeing automation frameworks without writing the tests myself. In 2026, while completing dual ISTQB AI Testing certifications (CT-AI and CT-GenAI), I decided to close the gap between strategy and execution.

This is an active learning project, not a production codebase. The goal is to understand Playwright deeply enough to make better architectural decisions and have more credible conversations with automation engineers — not to become a full-time SDET.

---

## What's in here

### Architecture

```
QAOpsPlaywright/
├── .github/workflows/          # CI/CD pipeline — GitHub Actions
├── features/                   # BDD feature files (Gherkin/Cucumber)
├── pageobjects/                # Page Object Model — JavaScript
├── pageobjects_ts/             # Page Object Model — TypeScript (migration)
├── tests/                      # Playwright test specs
├── utils/                      # Shared utilities — JavaScript
├── utils_ts/                   # Shared utilities — TypeScript
├── allure-report/              # Generated Allure HTML reports
├── allure-results/             # Raw Allure result data
├── playwright.config.js        # Base Playwright configuration
├── playwright.service.config.js# Cloud/service configuration
└── cucumber.js                 # Cucumber runner configuration
```

### What I built and why

**Page Object Model (POM) — JavaScript and TypeScript**
Starting in JavaScript, then migrating to TypeScript to understand the type-safety benefits in large test suites. At the bank, our Serenity BDD framework used a similar pattern — this gave me first-hand experience of why POM makes regression maintenance manageable at scale.

**BDD with Cucumber/Gherkin**
Feature files written in plain English business language, mapped to step definitions. This directly mirrors the Serenity BDD + Rest Assured framework I oversaw in production at Co-op Bank. Understanding how Gherkin scenarios translate to executable tests makes me a better Test Strategy author.

**GitHub Actions CI/CD Pipeline**
Automated test runs triggered on push/PR. The pipeline runs the full test suite and publishes an Allure report. At the bank, I owned the GitLab CI/CD test automation pipeline — this replicates that pattern in a GitHub context.

**Allure Reporting**
Rich HTML test reports with screenshots on failure, test history, and trend analysis. Understanding what good reporting looks like from the implementation side improves the governance standards I set for vendor QA teams.

**Dual configuration (base + service)**
Separate configs for local and cloud/service execution — learning how test environments need to be managed differently at scale.

---

## Key learning outcomes

- **BDD architecture**: How Gherkin feature files, step definitions, and Page Objects interact in a maintainable test suite
- **JS → TS migration**: Why TypeScript adoption in test frameworks reduces false failures and maintenance overhead
- **CI/CD integration**: How test pipelines are structured, what flaky test detection looks like at the pipeline level
- **Reporting**: What makes Allure reports actionable vs decorative
- **Environment management**: Multi-config approaches for local vs cloud test execution

---

## Tech stack

| Tool | Purpose |
|------|---------|
| [Playwright](https://playwright.dev/) | Cross-browser test automation |
| [Cucumber.js](https://cucumber.io/) | BDD framework / Gherkin runner |
| [Allure](https://allurereport.org/) | Test reporting |
| [GitHub Actions](https://github.com/features/actions) | CI/CD pipeline |
| TypeScript | Type-safe test code (migration from JS) |

---

## Background

This repo complements my professional certification work:
- **ISTQB AI Tester (CT-AI)** — April 2026
- **ISTQB Testing with Generative AI (CT-GenAI)** — May 2026

The certifications gave me the theoretical framework for AI in testing. This repo gives me the practical foundation to evaluate, govern, and improve automation work alongside the theory.

---

## Status

🟡 **Active learning project** — commits reflect the learning journey, not a finished product. Code quality and patterns improve across commits as understanding deepens.

---

*Connect on [LinkedIn](https://linkedin.com/in/shajimrankhan) or visit [shaj.uk](https://shaj.uk) for my full professional background.*
