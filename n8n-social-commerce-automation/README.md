# AI Social Commerce Automation with n8n

An n8n automation project for producing and managing short-form social-commerce content. It combines Shopee product data, AI-assisted content generation, video-processing APIs, and automated publishing workflows for TikTok shopping content. The same pipeline can support vertical AI storytelling, including Chinese-style short series, by generating scripts, visual prompts, captions, and sequential video assets.

## Workflows

### Shopee Product Video Automation

- Starts on a schedule and prepares product-oriented content.
- Uses AI models to analyze images and generate prompts, sales copy, and video content.
- Sends media-generation jobs to external APIs and checks their processing status.
- Stores workflow status and generated asset references in n8n Data Tables.
- Supports delivery to configured social-publishing integrations.

### TikTok Shopping Automation

- Receives product and user-generated-content data through webhooks.
- Analyzes product images and creates TikTok sales scripts with AI.
- Orchestrates image and video generation through asynchronous API requests.
- Tracks multiple processing stages, retries, and completion states.
- Prepares completed short-form videos for an automated TikTok shopping pipeline.

## Technologies

- n8n workflow automation
- OpenAI and Google Gemini nodes
- AI agents and structured-output parsers
- REST APIs and webhooks
- JavaScript processing nodes
- n8n Data Tables
- Scheduled triggers and asynchronous job polling
- Social-commerce and short-form video automation

## Repository Structure

```text
workflows/
├── shopee-video-automation.sanitized.json
└── tiktok-shopping-automation.sanitized.json
```

## Import and Setup

1. Import a sanitized JSON file into n8n.
2. Create your own credentials for every AI, HTTP, and publishing service.
3. Reconnect each node to the appropriate credential.
4. Review webhook paths, Data Table selections, API endpoints, and publishing settings.
5. Test each branch manually before activating its schedule or webhook in production.

## Security

The published workflows are portfolio-safe copies. Credential references and potentially sensitive authentication values were removed. The workflows are disabled by default and will not run until the owner supplies new credentials and completes configuration.

## Portfolio Summary

Designed an AI-assisted n8n automation pipeline for social-commerce video production. The system connects product inputs, image analysis, script and prompt generation, asynchronous media APIs, workflow-state tracking, and publishing preparation for Shopee and TikTok shopping content. It also supports vertical AI storytelling formats such as short Chinese-style series.

