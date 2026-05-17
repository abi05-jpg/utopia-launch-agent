## UTOPIA — Marketing & Events AI Agent

One-line: An AI agent that turns raw meeting transcripts into a LinkedIn post, follow-up email, and press angle using the LAUNCH framework.

## How to Run

1. Website: https://elaborate-kashata-e71762.netlify.app
2. n8n workflow is hosted on n8n Cloud (webhook endpoint receives POST requests)
3. Submit a transcript via the form → outputs appear on screen + logged to Google Sheets

## Architecture

Website (Netlify) → Webhook (n8n) → AI Agent (GPT-4o-mini) → Code Parser → Google Sheets → Response

## Prompt Used

### System Message:
You are the LAUNCH framework marketing agent for Utopia Studio. LAUNCH stands for Lead, Amplify, Unify, Nurture, Convert, Harvest.

When given a meeting transcript, immediately produce:

LINKEDIN_POST: A strong, opinionated LinkedIn post (150-200 words, includes CTA)
FOLLOW_UP_EMAIL: Personalised to the attendee, references specific transcript moments
PRESS_ANGLE: One sharp sentence a journalist could run with

### User Message:
Meeting Title: [title]
Date: [date]
Attendee: [name] ([email])
Transcript: [transcript]

## Tools & APIs

| Tool | Purpose |
|------|---------|
| n8n Cloud | Workflow orchestration |
| OpenAI GPT-4o-mini | Content generation |
| Google Sheets API | Output logging |
| Netlify | Frontend hosting |
| Lovable | Frontend builder |

## LAUNCH Framework

- **L**ead — Identify the sharpest insight
- **A**mplify — Turn it into a signal for LinkedIn/email/press
- **U**nify — Connect to Utopia's brand narrative
- **N**urture — Personalised follow-up
- **C**onvert — Drive next action
- **H**arvest — Extract press-ready angle
