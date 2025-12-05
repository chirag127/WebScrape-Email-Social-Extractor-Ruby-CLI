# WebScrape-Email-Social-Extractor-Ruby-CLI

![Build Status](https://img.shields.io/github/actions/workflow/user/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI/ci.yml?style=flat-square&logo=githubactions)
![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI?style=flat-square&logo=codecov)
![Ruby](https://img.shields.io/badge/Ruby-v3.2-red?style=flat-square&logo=ruby)
![SerpApi](https://img.shields.io/badge/SerpApi-integration-informational?style=flat-square&logo=serpapi)
![License](https://img.shields.io/github/license/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI?style=flat-square&logo=github)
![GitHub Stars](https://img.shields.io/github/stars/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI?style=flat-square&logo=github)

✨ **Elevate your lead generation and data intelligence.** This advanced Ruby CLI tool leverages Google Search results via SerpApi to precisely extract email addresses, social media handles, and other crucial information from websites.

🚀 **Instantly enrich your prospect lists and market research.**

---

## Table of Contents

*   [🚀 Key Features](#key-features)
*   [💡 Architecture](#architecture)
*   [✅ Getting Started](#getting-started)
*   [🛠️ Usage](#usage)
*   [📜 AGENTS.md Directives](#agentsmd-directives)
*   [⚖️ License](#license)

---

## 🚀 Key Features

*   **Automated Data Extraction:** Scrapes target websites efficiently.
*   **SerpApi Integration:** Utilizes powerful Google Search API for comprehensive results.
*   **Targeted Information:** Extracts emails, social media links (LinkedIn, Twitter, etc.), and custom data points.
*   **Ruby CLI Interface:** User-friendly command-line experience.
*   **Lead Generation Focused:** Designed to enhance sales and marketing outreach.
*   **Extensible Design:** Built with modularity for future enhancements.

---

## 💡 Architecture

mermaid
graph TD
    A[User Input CLI] --> B(Orchestrator Service)
    B --> C{SerpApi Client}
    C --> D[Google Search Results]
    D --> E(Data Parsing & Extraction Logic)
    E --> F(Email Extractor)
    E --> G(Social Media Extractor)
    E --> H(Custom Data Extractor)
    F --> I[Extracted Emails]
    G --> J[Extracted Social Handles]
    H --> K[Extracted Custom Data]
    I --> L(Output Formatter)
    J --> L
    K --> L
    L --> M[CLI Output / File]

    subgraph Core Logic
        E
        F
        G
        H
    end

    subgraph Integrations
        C
    end


This project adheres to a **Modular Monolith** architecture, ensuring a clear separation of concerns while maintaining a single deployable unit. Key components include the CLI interface, an orchestrator, the SerpApi integration client, and dedicated modules for parsing and extracting different data types.

---

## ✅ Getting Started

### Prerequisites

*   Ruby 3.2 or higher
*   Bundler (`gem install bundler`)
*   SerpApi API Key (obtain from [SerpApi](https://serpapi.com/)) - store this securely, e.g., in environment variables.

### Installation

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI.git
    cd WebScrape-Email-Social-Extractor-Ruby-CLI
    

2.  **Install dependencies:**
    bash
    bundle install
    

3.  **Set environment variable for SerpApi key:**
    bash
    export SERPAPI_API_KEY='YOUR_SERPAPI_API_KEY'
    
    *(Replace 'YOUR_SERPAPI_API_KEY' with your actual key)*

---

## 🛠️ Usage

Run the CLI tool with your desired target website or search query.

bash
bin/scrape --url <website_url>
# or
bin/scrape --query "search query for leads"


**Example:**

bash
bin/scrape --url https://example.com


**Options:**

*   `--url URL`: The website URL to scrape.
*   `--query "search query"`: A Google search query to find potential leads.
*   `--output FILE`: Optional file path to save the extracted data.
*   `--verbose`: Enable verbose logging.

---

## 📜 AGENTS.md Directives

<details>
<summary><strong>🤖 AI Agent Directives (December 2025 Standard)</strong></summary>

## SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

### 1. IDENTITY & PRIME DIRECTIVE

*   **Role:** Senior Principal Software Architect, Master Technical Copywriter.
*   **Experience:** 40+ years.
*   **Standards:** FAANG-level, "Managing the Unmanageable."
*   **Context Date:** December 2025 (building for 2026).
*   **Output:** EXECUTION-ONLY.
*   **Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

### 2. INPUT PROCESSING & COGNITION

*   **Speech-to-Text:** Infer technical intent over literal typos. Use `README.md` as SSOT.
*   **Mandatory MCP:** No guessing. Research (`brave`/`linkup`) industry standards, security threats, UI trends (Dec 2025). Verify APIs (`docfork`). Architect complex flows (`clear-thought-two`) *before* coding.

---

### 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)

*   **Project:** `WebScrape-Email-Social-Extractor-Ruby-CLI`
*   **Primary Scenario:** **DATA / SCRIPTS / WEB SCRAPING (Ruby)**
    *   **Stack:** **Ruby 3.2+**, **Bundler** (Package Management).
    *   **Linting/Formatting:** **RuboCop** (Industry standard for Ruby code quality).
    *   **Testing:** **RSpec** (Robust testing framework for Ruby).
    *   **Architecture:** **Modular Monolith**. Ensures clear separation of concerns (CLI, Orchestrator, SerpApi Client, Extraction Modules) within a single deployable unit.
    *   **External Integrations:** **SerpApi** for Google Search results.

---

### 4. DEVELOPMENT STANDARDS & VERIFICATION

*   **Code Quality:** Adhere strictly to **RuboCop** enforced style guides. Employ DRY, SOLID, KISS principles.
*   **Testing:** Comprehensive **RSpec** test suite covering all core functionalities, including integration with SerpApi (mocked where appropriate).
*   **Security:** Sensitive keys (e.g., SerpApi API Key) must **NEVER** be hardcoded. Utilize environment variables or secure secret management.
*   **Dependency Management:** Use **Bundler** exclusively. Ensure `Gemfile.lock` is committed.
*   **Verification Commands:**
    bash
    # Run linters and formatters
    bundle exec rubocop

    # Run tests
    bundle exec rspec
    

</details>

---

## ⚖️ License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license. See the [LICENSE](LICENSE) file for more details.

---

<div align="center">
  <p>Enjoy using the tool? Consider starring the repository!</p>
  <a href="https://github.com/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI/stargazers">
    <img src="https://img.shields.io/github/stars/chirag127/WebScrape-Email-Social-Extractor-Ruby-CLI?color=yellow&label=Star%20Me&logo=github&style=social" alt="Star Me on GitHub">
  </a>
</div>
