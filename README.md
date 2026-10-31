# Multi-Form Web Lead Deduplicator & Pipeline Console

## 🚀 Overview
An enterprise-grade Excel data cleaning and deduplication architecture designed to aggregate submissions across multiple web intake forms. This workbook normalizes raw lead streams, scrubs data via regular expressions, isolates duplicate entries, and routes clean leads directly to CRM platforms like Salesforce and HubSpot.

---

## 📑 Multi-Sheet Architectural Structure

1. **`01_Form_Response_Stream` (Tab 1)**
   * **Role:** Raw Multi-Form Intake Warehouse.
   * **Features:** Captures real-time form submissions across multiple source channels (`Web Form`, `Landing Page`, `Direct`, `Referral`) including raw timestamps, names, emails, phone numbers, and unique Submission IDs.

2. **`02_Regex_Scrubbing_Engine` (Tab 2)**
   * **Role:** Automated ETL & Scrubbing Layer.
   * **Features:** Standardizes names, validates email syntax, formats phone numbers, and scores individual row health.

3. **`03_Deduplication_Matrix` (Tab 3)**
   * **Role:** Lead Deduplication & Quarantine Engine.
   * **Features:** Tracks occurrence counts for email addresses, flags duplicate entries (`UNIQUE` vs `DUPLICATE`), and assigns automated CRM routing actions (`PASS TO CRM` or `QUARANTINE / IGNORE`).

4. **`04_Executive_Quality_Console` (Tab 4)**
   * **Role:** Executive Command Center & Export Portal.
   * **Features:** Displays live KPI summary scorecards (Total Leads Processed, Unique Clean Leads, Duplicates Filtered, and Data Health percentages) with 1-click CRM export readiness statuses.

---

## ⚙️ Technical Highlights
* **Multi-Channel Ingestion:** Seamlessly consolidates leads from disparate web intake forms into a unified schema.
* **Automated Deduplication:** Dynamic occurrence tracking that prevents redundant lead records from polluting sales pipelines.
* **Executive Visibility:** Real-time metrics dashboard designed for sales operations and data engineering leadership.
