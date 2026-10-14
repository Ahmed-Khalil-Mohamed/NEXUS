# Build from source — authorized maintainers

Application source is in the private `Ahmed-Khalil-Mohamed/NEXUS-source` repository. This public distribution repository cannot be built into NEXUS. Private access is required; a not-found response from GitHub is expected for accounts without access. End users should download an EXE from [Releases](https://github.com/Ahmed-Khalil-Mohamed/NEXUS/releases).

## Requirements and launch

Use Windows x64, Git, npm, and a supported Node.js release meeting the package's minimum of 22.13.0. The packaged desktop runtime is bundled separately by Electron. Authenticate Git through your own GitHub account; never paste a token into a clone URL or issue.

```powershell
git clone https://github.com/Ahmed-Khalil-Mohamed/NEXUS-source.git
cd NEXUS-source
npm ci
npm test
npm run build
npm run desktop
```

The tests exercise local functionality and test providers; they are not proof of the quality of every external AI response. Provider-specific integration checks need the respective CLI/service and its authentication.

## Package for Windows

```powershell
npm run desktop:build
```

This generates icons, builds the interface, and packages x64 NSIS and portable executables. The 0.6.6 package configuration outputs `release-v066/NEXUS-Setup-0.6.6.exe` and `release-v066/NEXUS-0.6.6-Windows.exe`. Current builds are unsigned; signing requires separately managed publisher credentials.

## Development commands

| Command | Purpose |
| --- | --- |
| `npm run dev` | Local backend and Vite development preview. |
| `npm run build` | TypeScript validation and frontend production build. |
| `npm start` | Backend and built interface. |
| `npm run desktop` | Electron desktop application. |
| `npm test` | Automated test suite. |
| `npm run agents:generate` | Regenerate the built-in role catalog. Review the output before committing. |

The browser preview lacks native Electron features such as Windows folder-picker IPC. Desktop builds should be smoke-tested independently.

## Source layout

| Directory | Responsibility |
| --- | --- |
| `desktop/` | Native window, splash, preload, and IPC. |
| `src/` | React UI, settings, conversations, and language handling. |
| `server/` | Local API, discovery, providers, orchestration, storage, and project handling. |
| `agents/` | Role definitions, Manager contract, schema, and catalog. |
| `tests/` | Local behavior and workflow verification. |
| `build/`, `public/` | Application icons and assets. |

## Publication boundary

Source changes stay in the private repository. The public repository contains documentation, campaign assets, and community templates, while EXEs are attached to Releases. Exclude `.nexus`, account credentials, `.env` files, local databases, dependency trees, and personal logs from source commits. Generate checksums and inspect release contents before distribution. This guide does not grant an open-source license or private repository access.
