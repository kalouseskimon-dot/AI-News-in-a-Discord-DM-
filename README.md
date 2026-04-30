# Autonomous AI News Synthesis & Delivery Pipeline

An enterprise-grade n8n workflow designed to aggregate, deduplicate, and synthesize artificial intelligence nomenclature and news from RSS feeds, delivering high-fidelity summaries via Discord Webhooks.

## 🚀 Architectural Overview
This pipeline leverages a multi-stage execution model:
1. **Ingestion**: Polls TechCrunch's AI RSS feed for the latest developments.
2. **Deduplication**: A custom JavaScript ephemeral state-check ensures only unique headlines are processed within a 5-item window.
3. **LLM Synthesis**: Utilizes **Google Gemini 1.5/2.0 Flash** via LangChain to perform semantic compression and impact analysis.
4. **Dispatch**: Formats and transmits a unified payload to a Discord destination.

## 🛠 Prerequisites
- **n8n Instance**: Self-hosted or Cloud.
- **Google AI Studio API Key**: For Gemini model access.
- **Discord Webhook**: For the final delivery endpoint.

## 📥 Installation
1. Download the `workflow.json` from this repository.
2. Open your n8n dashboard and select **Import from File**.
3. Configure your **Google Gemini(PaLM) Api** credentials within the AI Agent node.
4. Replace the `REDACTED` URL in the **HTTP Request** node with your actual Discord Webhook URL.

## ⚖️ License
Distributed under the [MIT License]. 
