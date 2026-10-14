# NEXUS 0.6.6 — A new home for your AI workflow

**A redesigned Home. Clearer model comparisons. A connected Store.**

NEXUS 0.6.6 brings a new visual direction to the Windows workspace, with warm neutral surfaces, petroleum-green accents and a calmer dark theme. This release also brings the Store and chat improvements developed since the previous public release, 0.5.1.

**[Download the Windows installer](https://github.com/Ahmed-Khalil-Mohamed/NEXUS/releases/download/v0.6.6/NEXUS-Setup-0.6.6.exe)** · **[Download the portable EXE](https://github.com/Ahmed-Khalil-Mohamed/NEXUS/releases/download/v0.6.6/NEXUS-0.6.6-Windows.exe)**

![NEXUS 0.6.6 Home in light mode](https://raw.githubusercontent.com/Ahmed-Khalil-Mohamed/NEXUS/v0.6.6/assets/v0.6.6/home-light.jpg)

## What's new in 0.6.6

- **Start directly from Home.** Write a draft, select Mix or a configured connection, then continue in Chat. Review your message and model before sending; continuing does not automatically call a provider.
- **Pick up where you left off.** Recent conversations sit alongside the composer, with quick access to the Store and workspace.
- **Compare one to three models.** Select models, set input/output token usage, and compare estimated API costs in readable cards. A searchable directory links to 26 companies' official pricing pages.
- **Read your AI briefing.** Follow selected companies and browse official announcements with publisher images where available. Missing images are labeled.
- **A more comfortable interface.** Refined light/dark colors, chat controls, spacing, short transitions, reduced-motion support and responsive English/Arabic layouts.

![Model comparison and API cost estimates](https://raw.githubusercontent.com/Ahmed-Khalil-Mohamed/NEXUS/v0.6.6/assets/v0.6.6/model-comparison.jpg)

Pricing is a dated snapshot, not a live quote. Cost bars compare the selected workload, not model quality. Check official rates before making a purchase; caching, tools, taxes and long-context surcharges are not included in the estimate.

## Also included since 0.5.1

### Store: skills, MCP tools and local models

- **Skills:** browse supported catalogs, select a detected compatible agent, review a skill and install its folder. Settings shows installed skills and their destinations. Installation depends on the target agent's supported skill format.
- **MCPs:** add ready connections such as Microsoft Learn, Cloudflare Docs, Context7 and Hugging Face, or use bundled Knowledge Memory and folder-scoped Project Filesystem. Search supported HTTP entries in the official MCP Registry. Discover tools and choose individual permissions before use.
- **AI Local:** explore public Hugging Face GGUF models, review publisher details and file sizes, then download a supported single-file model through Ollama. Follow progress, cancel, and use an installed model in Chat or Mix.

![MCP connections in the NEXUS Store](https://raw.githubusercontent.com/Ahmed-Khalil-Mohamed/NEXUS/v0.6.6/assets/v0.6.6/mcp-store.jpg)

Ollama must be installed for this local-model flow. Model architecture, hardware, license and tool support vary. Gated/private or split GGUF downloads are not supported. MCP OAuth sign-in is not supported in this release; adding a connection does not automatically grant tool permissions.

### Chat, API connections and Mix

- A unified conversation history replaces separate provider sections in the sidebar.
- Select the agent and model from the chat toolbar. Supported local and API connections can be used directly or together in Mix.
- Model choices come from the connection where supported; cached/default choices are labeled. Listing a model is not a successful inference check.
- Inspect Mix stages, assigned work, provider/model metadata, recorded instructions, activity and output. NEXUS Manager remains the coordinator.
- Refined profile, visual theme selection, language, API, MCP and team settings. Use @ in chat to reference available tools, skills or MCP tools.

![Updated NEXUS chat workspace](https://raw.githubusercontent.com/Ahmed-Khalil-Mohamed/NEXUS/v0.6.6/assets/v0.6.6/chat-light.jpg)

The 300 specialists are editable role definitions run through selected providers in scheduled batches, not 300 included models or 300 simultaneous calls. Availability, subscriptions and provider charges still apply.

## Updating from an earlier version

1. Finish your current work and close the old NEXUS window.
2. Back up your local workspace with NEXUS closed: `%APPDATA%/NEXUS/workspace`.
3. Run **NEXUS-Setup-0.6.6.exe**, or launch **NEXUS-0.6.6-Windows.exe** for portable use. Do not run the old and new versions together.
4. Confirm the displayed version is **0.6.6**. Existing profiles use local saved settings; the portable edition also stores data in the Windows profile.

Windows x64. Node.js is bundled. Startup includes the configured splash; the first portable extraction can take longer. Downloads are currently unsigned. Verify the source and hashes in [SHA256SUMS.txt](https://github.com/Ahmed-Khalil-Mohamed/NEXUS/releases/download/v0.6.6/SHA256SUMS.txt).

## Validation and release contents

- 73 automated tests passed; TypeScript, production build and packaging passed.
- Unpacked and portable Windows launch checks passed, including the frameless splash and visible main window.
- UI checks covered draft transfer, comparison limits/calculation/reset, recent conversations, both themes, Arabic RTL and narrow-window layouts.
- No live third-party inference was retested for the 0.6.6 visual changes. Test adapters are not evidence of 300 live model sessions.

The installer and portable EXE are accompanied by SHA-256 checksums and license notices. GitHub's automatic **Source code** archives contain this public repository's documentation and images, not the private application development source. Choose an **EXE** to run NEXUS.

Screenshots show the actual 0.6.6 interface through an isolated local preview. Alex and conversation titles are demonstration data; no AI responses or completed projects are fabricated. NEXUS is proprietary software and is not endorsed by the named providers.

**[Report a problem](https://github.com/Ahmed-Khalil-Mohamed/NEXUS/issues/new/choose)** · **[Read the user guide](https://github.com/Ahmed-Khalil-Mohamed/NEXUS/blob/main/docs/USER-GUIDE.md)**
