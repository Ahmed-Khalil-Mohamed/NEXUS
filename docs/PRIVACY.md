# Privacy and data handling

## Local storage

NEXUS 0.6.19 stores settings, chats, role edits, attachments, project records, scan progress, generated files, and backups under `%APPDATA%/NEXUS/workspace`. The portable edition uses the same location. Replacing an EXE does not erase the workspace. The conversation database and ordinary workspace files are not encrypted by NEXUS. Saved API keys and MCP bearer credentials use a separate Windows user-scoped DPAPI vault; copying that vault to a different Windows account does not make its credentials portable.

## AI requests

Sending a request shares relevant history, selected project context, and supported attachments with your chosen provider. Mix sends assignments and handoffs through its providers. Connection checks also invoke a provider. Its terms, retention policies, charges, and network behavior apply.

Local inference does not guarantee that every third-party tool is offline.

## News, catalogs and extensions

News retrieves official feeds and publisher images for the selected companies. Store browsing contacts the relevant skill catalogs, GitHub, the MCP Registry and Hugging Face. Local-model downloads are handled through Ollama and contact the model host. Provider/model catalogs contact the configured service where supported.

MCP tools may send their arguments to the selected server. Review the server and individual tool permissions before enabling them. Folder-scoped Filesystem tools operate on the folder you select; other MCP tools may have their own data handling. Skill installation writes the reviewed skill folder to the selected agent's supported location.

## Scans and projects

Discovery examines paths and registrations, not every personal document's content. It does not bypass Windows permissions or execute a discovered EXE. Project Lab reads bounded text content from a selected folder and excludes common secret filenames. Sensitive values inside normal code may still be included: inspect context before sending.

Custom connectors run with your Windows account. Use trusted tools and review their data behavior.

## Media

Attachments are stored locally and processed according to their type and provider support. Voice goes to your configured local transcription endpoint; resulting text can go to the AI provider. Video import samples three still frames.

## Public support

GitHub Issues are public. Redact tokens, private prompts, personal paths, and source. Never upload your workspace database or account configuration to a public issue.

## Source visibility

The public repository distributes documentation, screenshots, and release binaries. Source is stored separately in a private repository. Private visibility restricts public access; it does not mean GitHub has reviewed or certified the software and is not encryption of the executable.


## Pooled rooms

Local Pooled inference runs on this computer with a loopback signaling server and authenticated API bridge. Setup may contact upstream configuration or model-download services. Shared rooms use public signaling and trusted participating devices process model data associated with prompts and tool outputs. Invite keys remain in memory and are redacted from runtime logs. Do not send project context to untrusted rooms.
