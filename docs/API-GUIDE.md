# API & Advanced API guide

NEXUS 0.6.19 separates **chat connections** from **API research and activation guidance**. An API catalog entry does not become an executable tool simply by being listed.

## Connect a chat provider

1. Open **Settings → API connections** and choose a provider preset.
2. Enter a connection name, the provider's supported base URL, an authorized API key where required, and an available model ID.
3. Save and use the connection test. A test contacts the provider and may consume quota; check the returned result.
4. Choose the connection and model from the top picker in Chat, or include an eligible connection in your Mix routing preferences.

Saved connections are searchable. Editing and saving retains the same ID. Use the new-connection action for a separate record. Test feedback belongs to the current session, not a permanent guarantee of availability.

## Provider presets

The application includes 16 presets. Most use an OpenAI-compatible protocol; Anthropic uses its Messages protocol. Compatible protocols do not guarantee identical model features or tool support. Azure and Alibaba Cloud need your resource- or region-specific base URL. Use the official provider's documentation for available models and account requirements.

| Provider | Protocol | Official documentation |
| --- | --- | --- |
| OpenAI | openai | [Setup reference](https://platform.openai.com/docs/api-reference) |
| Anthropic | anthropic | [Setup reference](https://platform.claude.com/docs/en/api/overview) |
| Google Gemini | openai | [Setup reference](https://ai.google.dev/gemini-api/docs/openai) |
| Microsoft Azure | openai | [Setup reference](https://learn.microsoft.com/en-us/azure/developer/ai/how-to/switching-endpoints) |
| Mistral AI | openai | [Setup reference](https://docs.mistral.ai/api) |
| xAI | openai | [Setup reference](https://docs.x.ai/developers/rest-api-reference) |
| DeepSeek | openai | [Setup reference](https://api-docs.deepseek.com) |
| Cohere | openai | [Setup reference](https://docs.cohere.com/docs/compatibility-api) |
| NVIDIA | openai | [Setup reference](https://build.nvidia.com) |
| Hugging Face | openai | [Setup reference](https://huggingface.co/docs/inference-providers/en/tasks/chat-completion) |
| Groq | openai | [Setup reference](https://console.groq.com/docs/openai) |
| Together AI | openai | [Setup reference](https://docs.together.ai/docs/inference/openai-compatibility) |
| Fireworks AI | openai | [Setup reference](https://docs.fireworks.ai/tools-sdks/openai-compatibility) |
| OpenRouter | openai | [Setup reference](https://openrouter.ai/docs/api_reference/overview) |
| Cerebras | openai | [Setup reference](https://inference-docs.cerebras.ai/quickstart) |
| Alibaba Cloud / Qwen | openai | [Setup reference](https://www.alibabacloud.com/help/en/model-studio/compatibility-of-openai-with-dashscope) |

Custom compatible endpoints can also be configured. Services with other protocols need an adapter or a suitable MCP integration; listing a URL does not add protocol support.

## Advanced API workspace

Browse **138 service profiles across 16 categories**, with **12 handbook chapters**. Search, favorite entries, track activation steps and filter Chat connectors, Integration guides or My progress. Each card shows locally recorded checklist progress; details contain account requirements, setup links, credentials needed, monitoring guidance, caveats and references.

The application includes the original handbook PDF, Excel and JSON downloads. The public [catalog](API-CATALOG.md) and [JSON index](api-catalog.json) document every included service.

Nine handbook services map explicitly to NEXUS chat adapters: **Google Gemini, Groq, OpenRouter, Mistral, Cohere, Cerebras, Hugging Face, NVIDIA and OpenAI**. Other services are integration guidance, not automatically callable chat tools. This mapping count is separate from the 16 preset count.

Research snapshot: **2026-10-15**. Vendor prices, quotas and eligibility are not live verified. A Ready state or completed checklist records your progress, not external account activation.

## Google identity

[Configure a Desktop OAuth Client ID](GOOGLE-API-SETUP.md), then use the Google account area inside Advanced API. The distributed app does not include an operational project-owned Client ID. Real sign-in must be configured before use.

This is identity sign-in, not universal API authorization. Providers may still require their own consent, credentials, plans and billing. Google tokens are not forwarded to unrelated vendors.

## Credentials and usage

API keys and supported MCP bearer credentials use the Windows user-scoped DPAPI vault. Ordinary chat and workspace files are not encrypted by NEXUS. Do not include credentials in prompts, screenshots, public issues or checklist exports.

Activity reports use provider-reported usage where available; unknown token counts stay unknown. NEXUS's model price comparisons are estimates from dated snapshots, not invoices or live billing controls.

[MCP guide](MCP-GUIDE.md) · [Privacy](PRIVACY.md) · [Release notes](RELEASE-0.6.19.md)


## Using the full catalog in a project

[Detailed activation reference](API-ACTIVATION.md) lists every included service with its purpose, official setup page, credential type, checklist and caveats. For a chat-capable preset, create and test a connection. For other APIs, provide the agent with the official documentation and authorized project context, then implement the integration in your project or connect an appropriate MCP tool. Catalog membership alone does not give the agent live access.

[Pooled local inference](POOLED-GUIDE.md) is also available without a hosted chat-provider subscription; weights, hardware and upstream network requirements still apply.
