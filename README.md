# AI Agent News Summary Workflow

This repository contains an n8n workflow that automatically fetches world and technology news, uses an AI agent to summarise the headlines, and delivers a concise bullet‑point digest via email.

## Features

- **RSS Feed Integration:** Retrieves the latest world news from the BBC World News feed and technology news from The Verge.
- **AI Summarisation:** Utilises an OpenAI language model with a custom prompt to produce a succinct summary limited to ten bullet points and separated into "World news" and "Tech news" sections.
- **Email Delivery:** Sends the generated summary to a specified email address through the Gmail node.
- **Configurable:** Easily adjust RSS sources, summarisation parameters, and recipient address to match your needs.
- **n8n Native:** Designed as an importable `.json` workflow that runs on your self‑hosted or cloud n8n instance.

## Getting Started

1. **Prerequisites**
   - An [n8n](https://n8n.io/) instance (self‑hosted or Cloud).
   - A Gmail account configured in n8n (requires OAuth2 credentials).
   - An OpenAI API key configured in n8n as credentials for the LangChain nodes.

2. **Import the Workflow**
   - Download or clone this repository.
   - In the n8n UI, click **Import Workflow** and select `AI Agent workflow.json`.

3. **Configure Credentials**
   - Set up RSS, OpenAI and Gmail credentials according to your environment.
   - Update the `subject` and `recipient` fields in the "Send summary with Gmail" node if desired.

4. **Execute**
   - Trigger the workflow manually or schedule it using a Cron node to receive daily summaries.

## Customisation

- Change the RSS feed URLs in the "Get Tech News" and "Get World News" nodes to target your preferred sources.
- Modify the prompt text in the "AI Summary Agent" node to adjust tone, length or format.
- Add additional nodes (e.g. Slack, Telegram) to distribute the summary across other channels.

## License

This project is released under the MIT License. See the [LICENSE](LICENSE) file for details.
