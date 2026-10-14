# NEXUS user guide

[Home](../README.md) · [Downloads](https://github.com/Ahmed-Khalil-Mohamed/NEXUS/releases) · [FAQ](FAQ.md)

## Installation and first launch

Choose the Setup EXE for guided installation or the Windows EXE for portable use. Both contain the runtime. The portable edition stores data under `%APPDATA%/NEXUS/workspace`, not beside its EXE.

The frameless splash lasts approximately 30 seconds and follows the saved theme. Enter your name once, review discovered tools, select supported providers, and choose a team. Setup is saved between launches.

This preview is unsigned. Verify the release origin and compare the checksum without disabling Windows security:

```powershell
Get-FileHash "$env:USERPROFILE\Downloads\NEXUS-Setup-0.6.6.exe" -Algorithm SHA256
```

Compare with SHA256SUMS.txt from the same release. A matching hash confirms the bytes match the published release; it is not an independent security certification.

## Connect an AI provider

| Provider | Preparation |
| --- | --- |
| Codex CLI | Install and authenticate through the CLI's own sign-in flow. |
| Claude Code CLI | Install and authenticate through the CLI's own tools. |
| Ollama | Start its local service, make a model available, and select it in Settings. |
| LM Studio | Load a model, start its local API server, and configure it in Settings. |
| Custom local connector | Configure a supported local OpenAI-compatible service or CLI protocol and test it. |

Use **Settings → Tools & discovery** to manage providers and run connection checks. Checks send real short requests and can consume provider usage. Custom CLI tools run with your Windows permissions: configure trusted executables.

Detection, enablement, and readiness are separate. An arbitrary graphical app cannot execute work merely because its EXE is detected. In 0.6.6, Settings > API also supports compatible remote API connections with your own endpoint, model and credentials. Select a compatible protocol; a company preset does not guarantee every model supports chat or tools. Saved API keys use Windows user-scoped DPAPI protection.

## Home and model comparison

Write a draft on Home and select Mix or a configured connection. Continue opens Chat with the draft for review; it does not send a provider request. Recent conversations return you to saved work.

Choose AI interests for official announcements. The model explorer compares one to three selected models using a shared input/output token estimate. Prices are a dated snapshot, not live quotes; bars compare cost, not quality. Follow official links for current pricing.

## Store and extensions

- **Discover skills:** choose a supported catalog, review the skill and select a detected compatible agent. Settings > Skills lists installed items and destinations.
- **MCPs:** add a ready connection or search supported HTTP servers in the official registry. In Settings > MCP, discover tools and allow individual tools before use. Bundled Memory runs locally; Filesystem requires an allowed folder. OAuth sign-in is not supported.
- **AI Local:** browse Hugging Face models, review the publisher, license and file size, then download a supported public single-file GGUF through Ollama. Ollama must be installed. Use in chat becomes available after installation is confirmed; local connections can also join Mix. Hardware and tool capabilities vary.

Use @ in Chat to reference available tools, skills and MCP tools. Configuring a connection is not a guarantee that every model can execute every tool.

## Discovery

Quick discovery checks registered apps, known locations, and PATH. Deep scanning enumerates fixed local drives, supports pause/resume, and saves progress. It searches filenames and candidate definitions; it does not ingest all personal documents, bypass Windows permissions, or run discovered EXEs.

Protected paths and skipped links are reported. Display lists retain up to 1,000 entries per category while scanning continues. A candidate configuration is not proof of a runnable AI tool.

## Conversations

Select the agent and model in the top chat toolbar, start a chat, and add your task, optional project context, and attachments. Supported CLI, Local AI and API connections appear here. **Enter** sends; **Shift+Enter** adds a line. The composer expands with your text. The sidebar keeps a unified conversation history.

Use Direct chat for a provider conversation or Mix for coordinated work. Tool events are shown when reported by the integration; unavailable telemetry cannot be displayed.

Full conversation history stays local. Sent context is bounded to up to 20 recent messages within the selected 8,000 / 16,000 / 32,000-character allowance. Project context has a separate allowance. This is bounded context, not unlimited semantic memory.

## Project Lab and generated files

Select a folder or enter its path. Inspect the indexed files and suggested specialisms before sending. Folder selection alone does not send its content to a provider.

The reader processes up to **200 text files**, **500 KB total**, **100 KB per file**, and **12 levels** deep. It skips common secret filenames, binaries, dependency directories, and links. Sensitive values inside normal source files can still be included: inspect your context.

Generated changes appear in the report. **Apply** checks original file hashes, refuses conflicts, and saves backups before writing. Refresh the index after outside changes. Deletion is not supported by the apply protocol. Generated output is bounded to 30 files and 2 MB.

## Mix and the specialist library

The library contains 300 role definitions across 20 categories. Each describes scope, workflow, deliverables, permissions, and quality criteria. Roles are instruction contracts executed through your selected AI providers.

Choose specialists and providers. The fixed Manager plans assignments, dependencies, stages, and acceptance criteria. Large teams are planned in batches before the complete dependency plan is checked. Dependent tasks wait for prerequisites.

The Mix workflow rail shows recorded stages and assignment states. Select a step to inspect assigned work, instructions, activity, output and provider/model metadata. Instructions are sent prompts, not private model reasoning. Model names record the requested choice; an API may resolve aliases internally. A Mix team can consist entirely of supported Local AI and API connections.

NEXUS integrates contributions, reviews the result, and permits one repair/review pass when needed. Remaining issues are marked for follow-up. A failed specialist stops the run and cancels outstanding calls. Interrupted work is not silently resubmitted on restart.

All 300 roles can participate in scheduled batches. Concurrency is 1–4, not 300 simultaneous models. The normal budget is 24 calls, configurable up to 400; selecting the full team raises it to 350. Budgets are limits, not exact usage or outcome guarantees. Larger teams consume more provider usage.

Edit roles through simplified controls or JSON, import definitions, create roles, and restore saved versions. Changes are stored separately from the base catalog. The library supports up to 1,000 entries and teams up to 300. Editing is blocked during active work.

## Attachments and voice

| Input | Behavior |
| --- | --- |
| Text/code | Up to 100,000 extracted characters. |
| PDF | Text extraction from up to 100 pages; no scanned-image OCR. |
| DOCX | Text extraction. |
| PNG / JPEG / WebP | Vision input only with a compatible provider. |
| Video | Up to 200 MB; three frames at 10%, 50%, and 90%; no full-video or audio analysis. |
| Voice | Up to two minutes; requires a configured local transcription service. |

Messages accept up to eight attachments, with a 12 MB per-attachment limit. Claude CLI and plain-text custom connectors do not receive vision attachments in this version. Unsupported combinations report an error instead of pretending to understand them.

For voice, configure a local OpenAI-compatible `audio/transcriptions` endpoint and model in **Settings → General**. A recognition service is not installed automatically. Resulting text can become context for the chosen AI provider.

## Reports and response time

Expand a completed-run summary for duration, reported token counts, generated files, and outstanding issues. Previous reports remain with the chat.

Provider time includes transport, model processing, and its tool work. Local time covers preparation and bookkeeping. Tokens appear when reported; missing measurements are not invented.

AI review does not replace tests or a security audit. NEXUS does not automatically execute generated code or install dependencies. Review and test changes before deployment.

## Settings and updates

General contains your profile, language, theme, context allowance, and audio endpoint. Tools & discovery manages connections. Team & coordination controls execution preferences.

Back up `%APPDATA%/NEXUS/workspace` while NEXUS is closed before updating or changing machines. It contains private data and is not encrypted by NEXUS. Never attach it to public reports.

Download updates from Releases and close NEXUS before installing. No automatic updater is configured for this preview.
