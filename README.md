# 📡 Opp Nexus (`opp-nexus`)

> An automated career & opportunity aggregation engine powered by **n8n** and **LLM classification**. Tracks early-career job postings, industry conferences, free workshops, hackathons, and grants in a unified digest.

---

## 📊 Overview

Searching across scattered job boards, Luma/Eventbrite pages, tech conference listings, and community Discord servers is time-consuming. **Opp Nexus** automates this by pulling raw opportunity feeds into an **n8n automation pipeline**, filtering and tagging them using an LLM, and dispatching actionable digests to preferred channels (Discord, Slack, or Notion).

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
   git clone [https://github.com/](https://github.com/)<your-username>/opp-nexus.git
   cd opp-nexus


## 🚀 Development Roadmap (20+ Hours Planned Work)

### Phase 1: Ingestion & Trigger Workflows (~5 Hours)
- [ ] Build n8n cron triggers and HTTP Request nodes for Luma and Eventbrite endpoints.
- [ ] Implement web scrapers and RSS parsers in Python for tech conference and workshop directories.
- [ ] Build raw data sanitizer to clean HTML payloads before LLM evaluation.

### Phase 2: LLM Classification & Processing (~6 Hours)
- [ ] Design structured JSON extraction prompts to parse opportunity details (Title, Type, Deadline, Host, Location, Link).
- [ ] Implement deduplication nodes using fuzzy matching on event titles and URLs.
- [ ] Add domain relevance scoring to filter out low-value or spam postings automatically.

### Phase 3: Database & Notification Destinations (~5 Hours)
- [ ] Integrate Notion API node to store opportunities in a structured Kanban/List board.
- [ ] Build interactive Discord / Slack webhook templates with direct RSVP and application links.
- [ ] Set up automated calendar invite generation (.ics files) for workshop and conference deadlines.

### Phase 4: Testing & Analytics (~4 Hours)
- [ ] Create mock payload unit tests for edge cases (missing dates, expired links, multi-day events).
- [ ] Build dry-run pipeline tests in n8n.
- [ ] Create documentation for custom source additions and user filtering setup.