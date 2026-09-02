# Workflow Architecture Overview

This document describes the public, portfolio-safe architecture of the project. Production endpoints, account identifiers, webhook paths, affiliate links, credentials, and exported workflow JSON are intentionally excluded.

## Shopee Product Video Pipeline

1. A scheduled trigger starts the content-production cycle.
2. AI nodes analyze product images and generate structured prompts and sales content.
3. Batch and routing nodes prepare individual content jobs.
4. HTTP nodes submit image and video generation tasks to configured services.
5. Wait, switch, and condition nodes poll asynchronous job status.
6. Data Tables store asset references and processing states.
7. Completed media is prepared for configured social-publishing channels.

The production workflow contains 44 nodes.

## TikTok Shopping Video Pipeline

1. Webhooks receive product and UGC inputs.
2. AI vision analyzes the source image.
3. An AI agent produces a structured TikTok sales script.
4. Multiple media-generation stages create product-focused visual assets and video clips.
5. Conditional routing handles completion, retry, and failure states.
6. Data Tables maintain the state of every processing stage.
7. Finished assets are prepared for a TikTok shopping and product-tagging workflow.

The production workflow contains 48 nodes.

## Vertical AI Series Extension

The reusable AI content stages can also prepare vertical Chinese-style short-series content by changing the prompt templates and input assets. The pipeline can generate episodic scripts, character and scene prompts, vertical visual assets, captions, and sequential video jobs while reusing the same orchestration and status-tracking design.

## Security Design

- Secrets are stored in n8n Credentials, not in public documentation.
- Production webhooks and service endpoints are not published.
- Account, page, table, drive, and affiliate identifiers are excluded.
- Workflows should be tested manually before schedules or public webhooks are activated.
