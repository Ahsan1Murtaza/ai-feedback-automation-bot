# 📌 AI-Powered Multi-Year Feedback & Archival System

## 📖 Description
An enterprise-grade automation framework designed to manage, summarize, and archive student feedback across multiple academic years (First Year through Final Year). The system orchestrates data from various Google Form entry points, generates AI summaries for faculty, and consolidates all historical data into a single "Mega Archive" database.

The architecture follows a **Meta-Registry Pattern**, allowing for horizontal scaling (adding new years or departments) without modifying the core UiPath workflow.

## 🚀 Advanced Features
- **Multi-Year Orchestration:** Dynamically processes different academic years via a central Meta-Registry.
- **Mega Archive Consolidation:** Automatically moves processed feedback from year-specific tabs into a unified master database.
- **AI-Driven Faculty Reporting:** Generates intelligent summaries of student sentiment per teacher.
- **Non-Destructive Reset:** Clears response sheets while maintaining Google Form row integrity.
- **Scalable Teacher Onboarding:** Teacher-to-email mapping is handled at the sheet level—zero code changes required for staff updates.

## 🏗️ System Architecture
1. **Registry Scan:** Bot reads the `Meta_Registry` to identify `Active` years and their Spreadsheet IDs.
2. **Data Extraction:** Fetches new responses and teacher registries for each active year.
3. **Transformation:** - Maps diverse sheet columns to a unified Archive Schema.
    - Injects metadata (Academic Year, Archive Date).
4. **AI Processing:** Aggregates complaints per teacher and generates a weekly summary.
5. **Load & Purge:** - Appends normalized data to the `Mega_Archive_Database`.

## ⚙️ Tech Stack
- **UiPath (C# Modern Profile):** Core automation logic.
- **Google Workspace API:** Forms, Sheets, and Apps Script.
- **Generative AI:** For complaint summarization.
- **C# LINQ:** For high-speed data filtering and table manipulation.

## 📂 Design Principles
- **Zero-Hardcoding:** All paths, sheet names, and teacher lists are externalized.
- **Idempotency:** The bot can be re-run safely; it only processes and clears what is currently present.
- **Data Integrity:** Protects spreadsheet headers and Form metadata through range-specific cleansing.
