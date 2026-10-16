# Advanced API settings and Google setup

Open **Settings → API → Advanced API workspace** in NEXUS 0.6.13.

## Included

- 138 research profiles across 16 categories, searchable with locally saved favorites and activation checklists.
- Official setup links, account/credential requirements, allowance notes, billing conditions, monitoring guidance, minimum tests and source references.
- 12 handbook chapters, corrections, troubleshooting, glossary and the original PDF, Excel and JSON downloads.
- Nine explicit mappings to NEXUS chat adapters: Gemini, Groq, OpenRouter, Mistral, Cohere, Cerebras, Hugging Face, NVIDIA and OpenAI. Enter your authorized API key and the model ID supported by your account. Other catalog entries provide integration guidance; they are not automatically callable chat tools.
- Google identity sign-in prepared for a developer-owned Desktop OAuth client.

The supplied research is dated 2026-10-15. It is not a live entitlement, pricing or quota feed. Checklist completion and Ready are user-reported progress, not provider verification. Keys are stored through the existing Windows DPAPI vault, separately from checklist exports.

## Configure Google once

1. Create or select a project in [Google Cloud](https://console.cloud.google.com/auth/clients).
2. In Google Auth Platform, configure Branding, Audience and contact information. Add test users while the application is in testing.
3. Create an OAuth client with application type **Desktop app**.
4. Copy its **Client ID**, not an API key, password or client secret.
5. In NEXUS, open **Settings → API → Advanced API workspace → Google account → Developer setup**, paste the Client ID and save.
6. Select **Sign in with Google**, then **Open Google in browser**. Finish Google's consent flow and return to NEXUS.
7. Before distributing a configured build, review Google's publishing and verification requirements. A developer can supply the public client identifier with the `NEXUS_GOOGLE_CLIENT_ID` environment variable. Configuration entered in one local profile is not automatically embedded in distributed installers.

NEXUS uses the external system browser, a temporary `127.0.0.1` callback, state, PKCE S256 and a nonce. It verifies Google's signed identity token and stores credentials using Windows DPAPI. The callback expires after five minutes. Disconnect clears local credentials and attempts Google revocation; a failed remote revocation is reported.

Only `openid email profile` are requested. This is identity sign-in, not Gmail/Drive authorization or universal third-party API access. Provider setup pages may reuse the default browser's existing login session where supported; providers can still require their own consent, account, plan or API key. NEXUS does not extract cookies or forward Google tokens to other vendors.

Google sign-in was validated using a simulated OAuth server response and signed test identities. **Real Google login remains untested until a real Desktop Client ID is configured and authorized.**

Official references: [OAuth for installed applications](https://developers.google.com/identity/protocols/oauth2/native-app), [OpenID Connect](https://developers.google.com/identity/openid-connect/openid-connect).
