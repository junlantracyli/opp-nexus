# opp-nexus

# 📡 Career Radar (`career-radar`)

> An automated career opportunity aggregator powered by **n8n** and **LLM classification**. Tracks early-career job postings, industry conferences, free workshops, hackathons, and grants in a unified digest.

---

## 📊 Overview

Searching across scattered job boards, Luma/Eventbrite pages, tech conference listings, and community Discord servers is time-consuming. **Career Radar** automates this by pulling raw opportunity feeds into an **n8n automation pipeline**, filtering and tagging them using an LLM, and dispatching actionable digests to preferred channels (Discord, Slack, or Notion).

---

## 💡 Architecture & Key Features

* **Multi-Source Ingestion:** Scheduled n8n workflows fetch data from event APIs, tech RSS feeds, and company boards.
* **AI Opportunity Categorization:** LLMs classify incoming entries into standardized tags (`Job Role`, `Conference`, `Workshop`, `Hackathon`, `Grant`).
* **Smart Deduplication & Filtering:** Identifies duplicate posts and filters based on domain, experience level, and location (e.g., Remote, US-based).
* **Multi-Channel Alerts:** Sends formatted weekly/daily digests directly to Discord, Slack, or Notion with application and registration deadlines.

---

## 🛠 Tech Stack

* **Orchestration:** n8n (Self-hosted / Docker)
* **LLM Engine:** OpenAI / Anthropic / Gemini API
* **Backend Scripts:** Python 3.10+
* **Integrations:** Discord Webhooks, Notion API, Event/Job RSS Feeds

---

## 📋 Environment Setup

1. Clone the repository:
   ```bash
   git clone [https://github.com/](https://github.com/)<your-username>/career-radar.git
   cd career-radar