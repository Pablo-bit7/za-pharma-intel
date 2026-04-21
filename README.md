# ZA Pharma Intelligence Engine — Landing Page

A product landing page for an AI-powered pharmaceutical market intelligence platform built on a live MCP (Model Context Protocol) server, designed to surface regulatory, procurement, and pricing insights from South Africa's national pharmaceutical data ecosystem.

---

## Overview

South Africa's pharmaceutical landscape is governed by a fragmented set of public data sources — SAHPRA's regulatory registry, the NDoH's Master Health Product List, and the Medicine Price Registry — none of which communicate with each other out of the box. The result is that market access analysts, regulatory professionals, and supply chain teams spend hours manually reconciling data that should be instantly queryable.

The **ZA Pharma Intelligence Engine** solves this by exposing a FastMCP server that bridges these three silos and makes them queryable through natural language inside Claude. This landing page communicates that product vision to potential pilot users, documents the architecture, and drives access key requests from target personas.

---

## Key Features

### Product Communication
- Clear articulation of the problem (disconnected data silos) and the solution (a unified MCP intelligence layer)
- Architecture walkthrough explaining the ingestion pipeline, normalization logic, and just-in-time cross-referencing
- Transparent framing of current constraints (LLM context window throttling) and the roadmap to vector store retrieval

### Interactive Architecture Section
- Tabbed walkthrough of the four-stage pipeline: Ingestion → Harmonization → Verification → Just-in-Time Intel
- Each stage explained in plain language for both technical and non-technical stakeholders

### Live Data Visualizations
- **Market Parity Chart**: Bar chart comparing average NDoH public tender unit prices vs. private sector Single Exit Prices (SEP), demonstrating pricing disparity
- **Audit Donut Chart**: Visualizes SAHPRA license verification rates across a sample of tender awardees, surfacing unverified supplier profiles

### Pilot Access Flow
- Dual CTA structure targeting new users (Access Key requests) and active pilot testers (Feedback submission)
- Webhook-ready anchor links for n8n automation integration

---

## Tech Stack

| Layer | Technology |
|---|---|
| Markup & Layout | HTML5, Tailwind CSS (CDN) |
| Data Visualization | Chart.js |
| Typography | Inter (Google Fonts) |
| Interactivity | Vanilla JavaScript |
| Backend (MCP Server) | Python, FastMCP, httpx, pandas |
| Automation (Pilot Flow) | n8n (webhook endpoints) |

---

## Usage

The landing page is a single self-contained `index.html` file with no build step required.

```bash
# Clone the repository
git clone https://github.com/your-username/za-pharma-intel.git
cd za-pharma-intel

# Open directly in browser
open index.html

# Or serve locally
python3 -m http.server 8080
```

---

## What This Demonstrates

This project reflects a systems-level approach to building and communicating technical products:

- **Full-stack thinking**: The landing page is the front door to a live backend MCP server (`server.py`) with real data pipelines (`mhpl_utils.py`, `mpr_utils.py`, `sahpra_utils.py`). The UI was designed with genuine knowledge of what the system actually does.
- **Data pipeline literacy**: Understanding of how to ingest, normalize, and cross-reference heterogeneous government datasets across regulatory, procurement, and pricing domains.
- **Product communication**: Ability to translate complex backend architecture (MCP, LLM context windows, vector stores) into clear, scannable content for both technical and business audiences.
- **Automation integration**: Designed with n8n webhook endpoints in mind, enabling a fully automated pilot onboarding and feedback loop without manual intervention.

---

## Author

**Paballo Mogane**
Junior Python Developer | Automation Engineer
