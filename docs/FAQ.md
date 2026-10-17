# Frequently asked questions

## Which download runs NEXUS?

Choose **NEXUS-Setup-0.6.19.exe** to install or **NEXUS-0.6.19-Windows.exe** for portable use. No source archive, development tools, or separate Node.js installation is needed.

## Why does GitHub show Source code downloads?

GitHub adds ZIP/TAR archives automatically. Here they contain documentation and images, not NEXUS development source. Choose an EXE for the program.

## Is it open source?

No. Source is private and binaries have a proprietary notice. Third-party components retain their own licenses. A locally installed binary can still be inspected or reverse engineered; private source hosting does not make the executable impossible to inspect.

## Are AI subscriptions or models included?

No. Connect a supported provider or local model service. Its charges and quotas apply.

## Are there 300 separate AI models?

There are 300 specialist role definitions working through selected providers in batches, with up to four concurrent calls.

## Why is a detected app not runnable?

Execution needs a supported, configured CLI or API and authentication where required. Use the connection test in Settings.

## Why does startup take 30 seconds?

The splash deliberately lasts about 30 seconds. This is separate from AI response time.

## Why is a response slow?

Expand the run report to compare provider time and local time. Provider latency includes transport, model processing, and tool work. Larger Mix teams require more calls. Select a smaller suitable team for simpler tasks.

## Does scanning read all my documents?

No. Deep discovery enumerates filenames. Project content is read separately from a chosen folder, within limits. Windows permissions apply.

## Why is voice transcription unavailable?

It needs microphone access and a configured local transcription service, which NEXUS does not install automatically.

## Does it execute generated code automatically?

Generated code is not automatically executed or installed. File delivery can be automatic or require review, according to chat preferences; conflict checks and backups apply to either mode. The file-delivery protocol does not delete project files.

## Why does Windows show an unknown publisher?

This preview is unsigned. Verify its origin and SHA-256 checksum; do not disable Windows security.

## Where are my portable edition chats?

In `%APPDATA%/NEXUS/workspace`, not beside the EXE. Back up this folder with NEXUS closed before moving devices.
