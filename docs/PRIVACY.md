# Privacy and data handling

## Local storage

NEXUS 0.5.1 stores settings, chats, role edits, attachments, project records, scan progress, generated files, and backups under `%APPDATA%/NEXUS/workspace`. The portable edition uses the same location. Replacing an EXE does not erase the workspace. SQLite and accompanying files are not encrypted by NEXUS.

## AI requests

Sending a request shares relevant history, selected project context, and supported attachments with your chosen provider. Mix sends assignments and handoffs through its providers. Connection checks also invoke a provider. Its terms, retention policies, charges, and network behavior apply.

Local inference does not guarantee that every third-party tool is offline.

## Scans and projects

Discovery examines paths and registrations, not every personal document's content. It does not bypass Windows permissions or execute a discovered EXE. Project Lab reads bounded text content from a selected folder and excludes common secret filenames. Sensitive values inside normal code may still be included: inspect context before sending.

Custom connectors run with your Windows account. Use trusted tools and review their data behavior.

## Media

Attachments are stored locally and processed according to their type and provider support. Voice goes to your configured local transcription endpoint; resulting text can go to the AI provider. Video import samples three still frames.

## Public support

GitHub Issues are public. Redact tokens, private prompts, personal paths, and source. Never upload your workspace database or account configuration to a public issue.

## Source visibility

The public repository distributes documentation, screenshots, and release binaries. Source is stored separately in a private repository. Private visibility restricts public access; it does not mean GitHub has reviewed or certified the software and is not encryption of the executable.
