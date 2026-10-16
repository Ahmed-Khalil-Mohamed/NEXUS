# API service catalog — 138 profiles

Included in **Settings → API connections → Advanced API workspace**. Research snapshot: **2026-10-15**. Prices, quotas, eligibility and policies can change. Follow official setup pages.

Nine entries have explicit chat mappings; others are integration guides needing an appropriate implementation. Checklist progress is not proof of activation. See the [API guide](API-GUIDE.md) and [JSON catalog](api-catalog.json).

## AI and LLMs

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API001 | [Google Gemini API](https://aistudio.google.com/app/apikey) | Add text generation, summarization, structured extraction and multimodal understanding to an application. | Chat connector |
| API002 | [Groq API](https://console.groq.com/keys) | Run supported language models and speech recognition without hosting inference hardware. | Chat connector |
| API003 | [OpenRouter Free](https://openrouter.ai/settings/keys) | Access multiple model providers through one integration and evaluate free model routes. | Chat connector |
| API004 | [Mistral AI API](https://console.mistral.ai/api-keys) | Add chat, coding, text analysis and supported document capabilities through a hosted API. | Chat connector |
| API005 | [Cloudflare Workers AI](https://dash.cloudflare.com/) | Run eligible AI models close to your application using Workers bindings or REST. | Integration guide |
| API006 | [OpenAI Moderation API](https://platform.openai.com/api-keys) | Classify potentially harmful text and image content as one component of application safety. | Integration guide |
| API007 | [Cohere Evaluation API](https://docs.cohere.com/docs/rate-limits) | Evaluate language, retrieval and related AI capabilities before selecting a production plan. | Chat connector |
| API008 | [Cerebras Inference](https://inference-docs.cerebras.ai/support/rate-limits) | Evaluate hosted inference and compare its behavior with other model providers. | Chat connector |
| API009 | [Hugging Face Inference Providers](https://huggingface.co/settings/tokens) | Try multiple hosted model providers using a Hugging Face access token. | Chat connector |
| API010 | [Z.AI / Zhipu](https://docs.z.ai/guides/overview/pricing) | Evaluate the specific Flash text or vision models that the relevant platform lists as free. | Integration guide |
| API011 | [Aion Labs](https://www.aionlabs.ai/docs/rate-limits/) | Evaluate supported text-generation models for a small prototype. | Integration guide |
| API012 | [Kilo AI Gateway](https://kilo.ai/docs/gateway/authentication) | Experiment with eligible free models through a gateway, including an anonymous access path. | Integration guide |
| API013 | [LLM7.io](https://docs.llm7.io/limits) | Try a limited hosted model gateway using its current token-based access. | Integration guide |
| API014 | [ModelScope](https://www.modelscope.ai/docs/model-service/API-Inference/limits) | Investigate models exposed through ModelScope API-Inference. | Integration guide |
| API015 | [NVIDIA NIM](https://docs.api.nvidia.com/nim/docs/product) | Evaluate NVIDIA-hosted model endpoints and assess a later self-hosted NIM deployment. | Chat connector |
| API016 | [Ollama Cloud](https://docs.ollama.com/cloud) | Use hosted models when local hardware is insufficient. | Integration guide |
| API017 | [OVHcloud AI Endpoints](https://docs.ovhcloud.com/en/guides/public-cloud/ai-machine-learning/ai-endpoints-getting-started) | Evaluate hosted AI endpoints through anonymous testing or a provisioned cloud project. | Integration guide |
| API018 | [SiliconFlow](https://docs.siliconflow.cn/cn/usercases/use-siliconcloud-in-ccswitch) | Investigate hosted open-model inference on the platform available to your region. | Integration guide |
| API019 | [OpenAI Generative API](https://platform.openai.com/api-keys) | Build text, image and audio features using paid API products and available account entitlements. | Chat connector |
| API020 | [GitHub Models](https://docs.github.com/en/github-models) | Historical directory entry retained so old tutorials are not mistaken for an available integration. | Integration guide |

## Translation, speech and OCR

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API021 | [Azure AI Translator](https://azure.microsoft.com/en-us/pricing/details/translator/) | Translate application text, detect language and use supported dictionary or transliteration functions. | Integration guide |
| API022 | [Azure AI Speech](https://azure.microsoft.com/en-us/pricing/details/speech/) | Convert audio to text and text to neural speech for an application. | Integration guide |
| API023 | [Google Cloud Text-to-Speech](https://cloud.google.com/text-to-speech/pricing) | Generate speech from text for reading, accessibility and voice responses. | Integration guide |
| API024 | [Google Cloud Vision](https://cloud.google.com/vision/pricing) | Extract printed text and detect supported visual features in images. | Integration guide |
| API025 | [Google Cloud Translation (NMT)](https://docs.cloud.google.com/translate/docs/setup) | Provide managed text translation inside a backend. | Integration guide |
| API026 | [OCR.Space](https://ocr.space/ocrapi) | Convert supported image or PDF text into machine-readable output. | Integration guide |
| API027 | [ElevenLabs API Free](https://elevenlabs.io/pricing) | Prototype supported speech generation and voice features. | Integration guide |
| API028 | [DeepL API Free / Developer](https://support.deepl.com/hc/en-us/articles/360021200939-DeepL-API-plans) | Evaluate text translation through an API, while separating legacy and new account plans. | Integration guide |
| API029 | [MyMemory](https://mymemory.translated.net/doc/usagelimits.php) | Add lightweight translation to small applications or prototypes. | Integration guide |
| API030 | [Deepgram](https://deepgram.com/pricing) | Evaluate speech recognition and other supported speech APIs. | Integration guide |

## Web search and extraction

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API031 | [Brave Search API](https://brave.com/search/api/) | Add search results to an application or AI research workflow. | Integration guide |
| API032 | [Tavily API](https://www.tavily.com/pricing) | Retrieve web results and evidence for AI-assisted research. | Integration guide |
| API033 | [Exa API](https://exa.ai/pricing) | Find semantically relevant pages and retrieve their content. | Integration guide |
| API034 | [Firecrawl API](https://www.firecrawl.dev/pricing) | Extract web pages as Markdown or structured data for indexing and retrieval. | Integration guide |
| API035 | [Jina Reader API](https://jina.ai/reader/) | Convert a URL into readable content for an AI or search pipeline. | Integration guide |
| API036 | [SerpApi](https://serpapi.com/pricing) | Receive search-engine results as structured JSON. | Integration guide |

## Databases and backend

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API037 | [Supabase](https://supabase.com/pricing) | Build a PostgreSQL-backed app with authentication, storage, REST access and realtime features. | Integration guide |
| API038 | [Firebase / Cloud Firestore](https://firebase.google.com/pricing) | Store application documents with SDK synchronization and controlled client access. | Integration guide |
| API039 | [Neon Postgres](https://neon.com/pricing) | Run managed PostgreSQL without administering a database VM. | Integration guide |
| API040 | [Upstash Redis REST](https://upstash.com/pricing/redis) | Add caching, counters, sessions and application rate limits. | Integration guide |
| API041 | [Appwrite Cloud](https://appwrite.io/pricing) | Use managed accounts, databases, file storage, functions and realtime services. | Integration guide |
| API042 | [Qdrant Cloud](https://qdrant.tech/pricing/) | Store embeddings for semantic search and retrieval-augmented generation. | Integration guide |
| API043 | [Pinecone Starter](https://www.pinecone.io/pricing/) | Host vector or hybrid search indexes for retrieval and recommendations. | Integration guide |
| API044 | [Cloudflare D1](https://developers.cloudflare.com/d1/platform/pricing/) | Store SQL data for a Workers-based backend. | Integration guide |
| API045 | [Turso](https://turso.tech/pricing) | Use managed SQLite/libSQL databases for lightweight distributed applications. | Integration guide |
| API046 | [Cloudflare Workers KV](https://developers.cloudflare.com/kv/platform/pricing/) | Store configuration, cached values and simple key-value data at the edge. | Integration guide |
| API047 | [Cloudflare Workers](https://developers.cloudflare.com/workers/platform/pricing/) | Deploy HTTP endpoints, backend logic and edge request processing. | Integration guide |

## Identity and security

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API048 | [Firebase Authentication](https://firebase.google.com/pricing) | Manage application users and supported sign-in providers. | Integration guide |
| API049 | [Clerk](https://clerk.com/pricing) | Add user sessions, hosted sign-in screens and account management. | Integration guide |
| API050 | [Auth0](https://auth0.com/pricing) | Provide OAuth/OIDC login, identity federation and token-based application access. | Integration guide |
| API051 | [Cloudflare Turnstile](https://developers.cloudflare.com/turnstile/plans/) | Reduce automated abuse of forms, login and account creation. | Integration guide |
| API052 | [HIBP Pwned Passwords](https://haveibeenpwned.com/API/V3) | Check whether a password hash prefix appears in the breach corpus. | Integration guide |

## Email, notifications and realtime

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API053 | [Resend](https://resend.com/pricing) | Send transactional email such as verification messages and receipts. | Integration guide |
| API054 | [Mailjet](https://www.mailjet.com/pricing/) | Send application email through an API or SMTP. | Integration guide |
| API055 | [Firebase Cloud Messaging](https://firebase.google.com/pricing) | Deliver push notifications to registered Android, iOS and web app instances. | Integration guide |
| API056 | [Telegram Bot API](https://core.telegram.org/bots/faq) | Build bot commands, customer-service interactions and operational notifications inside Telegram. | Integration guide |
| API057 | [Discord API / Webhooks](https://docs.discord.com/developers/resources/webhook) | Send team alerts or build community bot integrations. | Integration guide |
| API058 | [Pusher Channels](https://pusher.com/channels/pricing/) | Publish live chat events, presence and interface updates. | Integration guide |
| API059 | [Ably](https://ably.com/pricing) | Synchronize application events, chat and presence over managed realtime channels. | Integration guide |
| API060 | [OneSignal](https://onesignal.com/pricing) | Manage push delivery and targeted messaging across supported channels. | Integration guide |
| API061 | [Brevo Email API](https://www.brevo.com/features/email-api/) | Send verification, order and other transactional emails. | Integration guide |
| API062 | [Daily Video API](https://www.daily.co/pricing/video-sdk/) | Embed voice/video rooms and participant sessions in an app. | Integration guide |
| API063 | [Twilio SMS / Voice](https://www.twilio.com/docs/usage/tutorials/how-to-use-your-free-trial-account) | Evaluate SMS verification, messaging or programmable voice. | Integration guide |

## Storage and media

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API064 | [Cloudflare R2](https://developers.cloudflare.com/r2/pricing/) | Store files and objects using an S3-compatible interface. | Integration guide |
| API065 | [Firebase Cloud Storage](https://firebase.google.com/docs/storage/faqs-storage-changes-announced-sept-2024) | Store user uploads and application media with Firebase access controls. | Integration guide |
| API066 | [Cloudinary](https://cloudinary.com/pricing) | Upload, transform, optimize and deliver images or video. | Integration guide |
| API067 | [ImageKit](https://imagekit.io/plans/) | Optimize media and provide responsive image/video delivery. | Integration guide |
| API068 | [Unsplash API](https://unsplash.com/documentation) | Search and display photographic images with creator metadata. | Integration guide |
| API069 | [Pixabay API](https://pixabay.com/api/docs/) | Search supported images, illustrations and videos. | Integration guide |
| API070 | [Openverse API](https://docs.openverse.org/api/reference/authentication_and_throttling.html) | Discover images and audio with open-license metadata. | Integration guide |
| API071 | [Pexels API](https://www.pexels.com/api/) | Search photo and video assets for supported application experiences. | Integration guide |

## Maps and geolocation

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API072 | [Geoapify](https://www.geoapify.com/pricing/) | Add geocoding, routes, places and mapping functions. | Integration guide |
| API073 | [LocationIQ](https://locationiq.com/pricing) | Convert addresses to coordinates and coordinates to addresses. | Integration guide |
| API074 | [Nominatim - OSM public server](https://operations.osmfoundation.org/policies/nominatim/) | Perform low-volume address search against OpenStreetMap data. | Integration guide |
| API075 | [TomTom Maps APIs](https://docs.tomtom.com/pricing) | Use maps, routing, geocoding and traffic data. | Integration guide |
| API076 | [Google Maps Platform](https://developers.google.com/maps/billing-and-pricing/pricing) | Add maps, routes, places and distance-related functions to an application. | Integration guide |
| API077 | [Mapbox APIs](https://www.mapbox.com/pricing) | Build styled maps, search and navigation experiences. | Integration guide |
| API078 | [GeoNames](https://www.geonames.org/export/web-services.html) | Look up place names and geographic reference data. | Integration guide |
| API079 | [IPinfo Lite](https://ipinfo.io/pricing) | Enrich an IP address with basic network/country information. | Integration guide |
| API080 | [REST Countries](https://restcountries.com/plans) | Retrieve country names, codes, languages, currencies and related reference fields. | Integration guide |
| API081 | [ipify](https://www.ipify.org/) | Return the public IPv4/IPv6 address visible to the service. | Integration guide |
| API082 | [OpenCage Free Trial](https://opencagedata.com/pricing) | Evaluate forward and reverse geocoding. | Integration guide |

## Weather and environment

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API083 | [Open-Meteo](https://open-meteo.com/en/pricing) | Retrieve weather forecasts and supported historical or environmental datasets. | Integration guide |
| API084 | [OpenWeather](https://openweathermap.org/price) | Display current conditions and selected forecast products. | Integration guide |
| API085 | [WeatherAPI.com](https://www.weatherapi.com/) | Add weather, forecasts and related location data to an application. | Integration guide |
| API086 | [OpenAQ API v3](https://docs.openaq.org/using-the-api/api-key) | Read air-quality observations and station metadata. | Integration guide |
| API087 | [Tomorrow.io](https://support.tomorrow.io/hc/en-us/articles/20273728362644-Free-API-Plan-Rate-Limits) | Add weather conditions and forecasts to location-aware applications. | Integration guide |

## Currencies and finance data

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API088 | [Frankfurter API](https://frankfurter.dev/) | Convert reference currency values and retrieve historical rates. | Integration guide |
| API089 | [ExchangeRate-API Open](https://www.exchangerate-api.com/docs/free) | Use periodically updated currency conversion tables. | Integration guide |
| API090 | [CoinGecko Demo API](https://www.coingecko.com/en/api/pricing) | Read cryptocurrency prices and market metadata for a prototype. | Integration guide |
| API091 | [Alpha Vantage](https://www.alphavantage.co/support/) | Retrieve selected market time series and technical indicator data. | Integration guide |
| API092 | [Twelve Data Basic](https://twelvedata.com/pricing) | Prototype financial market data queries and indicators. | Integration guide |
| API093 | [Stripe Sandbox](https://docs.stripe.com/sandboxes) | Test payment flows, webhooks and failure handling without moving real money. | Integration guide |

## Developer and workspace integrations

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API094 | [GitHub REST API](https://docs.github.com/en/rest/using-the-rest-api/rate-limits-for-the-rest-api) | Read repository metadata and automate issues, pull requests and releases with appropriate permissions. | Integration guide |
| API095 | [Google Sheets API](https://console.cloud.google.com/apis/library/sheets.googleapis.com) | Read/write spreadsheet data and automate reports with owner-authorized access. | Integration guide |
| API096 | [Google Docs API](https://console.cloud.google.com/apis/library/docs.googleapis.com) | Create and modify native documents programmatically. | Integration guide |
| API097 | [Google Drive API](https://console.cloud.google.com/apis/library/drive.googleapis.com) | List, upload, organize and share files under an authorized identity. | Integration guide |
| API098 | [Google Calendar API](https://console.cloud.google.com/apis/library/calendar-json.googleapis.com) | Read availability and manage events on calendars the identity can access. | Integration guide |
| API099 | [Gmail API](https://console.cloud.google.com/apis/library/gmail.googleapis.com) | Read or send email and manage labels with the mailbox owner's permission. | Integration guide |
| API100 | [YouTube Data API](https://console.cloud.google.com/apis/library/youtube.googleapis.com) | Read video/channel metadata and perform authorized channel-management operations. | Integration guide |
| API101 | [Google Books API](https://console.cloud.google.com/apis/library/books.googleapis.com) | Find book metadata, covers and supported previews. | Integration guide |

## Testing and educational APIs

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API102 | [JSONPlaceholder](https://jsonplaceholder.typicode.com/) | Prototype lists, users and HTTP CRUD interactions without building a backend. | Integration guide |
| API103 | [DummyJSON](https://dummyjson.com/docs) | Build product, cart and user interfaces with realistic sample structures. | Integration guide |
| API104 | [Random User Generator](https://randomuser.me/documentation) | Populate UI prototypes with synthetic-looking user records. | Integration guide |
| API105 | [httpbin](https://httpbin.org/) | Inspect HTTP requests, headers, redirects and status-code handling. | Integration guide |
| API106 | [PokeAPI](https://pokeapi.co/docs/v2) | Explore a structured dataset while learning REST or building fan-oriented prototypes. | Integration guide |
| API107 | [Open Trivia DB](https://opentdb.com/api_config.php) | Retrieve categorized quiz questions for an educational prototype. | Integration guide |
| API108 | [Free Dictionary API](https://dictionaryapi.dev/) | Display supported English definitions, pronunciations and example usage. | Integration guide |
| API109 | [Datamuse](https://www.datamuse.com/api/) | Find related words, rhymes and suggestions for writing or word games. | Integration guide |

## Research and public datasets

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API110 | [Crossref REST API](https://www.crossref.org/documentation/retrieve-metadata/rest-api/) | Resolve DOI metadata and build reference or citation workflows. | Integration guide |
| API111 | [OpenAlex API](https://openalex.org/pricing) | Analyze scholarly works, authors, institutions and citation relationships. | Integration guide |
| API112 | [NASA Open APIs](https://api.nasa.gov/) | Build educational astronomy, image or space-data features. | Integration guide |
| API113 | [World Bank Indicators API](https://datahelpdesk.worldbank.org/knowledgebase/articles/889392-about-the-indicators-api-documentation) | Retrieve country-level economic, demographic and development indicators. | Integration guide |
| API114 | [Open Library APIs](https://openlibrary.org/developers/api) | Retrieve book, edition, author and cover metadata. | Integration guide |
| API115 | [USGS Earthquake API](https://earthquake.usgs.gov/fdsnws/event/1/) | Query earthquake events by place, time, magnitude and depth. | Integration guide |
| API116 | [USDA FoodData Central](https://fdc.nal.usda.gov/api-guide/) | Search food records and nutrient data for an application. | Integration guide |
| API117 | [NHTSA vPIC](https://vpic.nhtsa.dot.gov/api/) | Decode VINs and retrieve manufacturer or vehicle reference information. | Integration guide |

## Media, news and specialist data

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API118 | [TMDB API](https://developer.themoviedb.org/docs/faq) | Build film/TV metadata, poster and cast discovery interfaces. | Integration guide |
| API119 | [TVmaze API](https://www.tvmaze.com/api) | Retrieve television series, episode and schedule metadata. | Integration guide |
| API120 | [football-data.org](https://www.football-data.org/pricing) | Display covered fixtures, standings and teams. | Integration guide |
| API121 | [Open Food Facts](https://openfoodfacts.github.io/openfoodfacts-server/api/) | Look up community food product data by barcode. | Integration guide |
| API122 | [Currents News API](https://currentsapi.services/en) | Retrieve headlines and news-search metadata for a prototype. | Integration guide |
| API123 | [NewsAPI Developer](https://newsapi.org/pricing) | Prototype news-headline search during development. | Integration guide |

## Islamic reference services

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API124 | [AlAdhan API](https://aladhan.com/prayer-times-api) | Calculate prayer times for a chosen location and date. | Integration guide |
| API125 | [AlQuran Cloud API](https://alquran.cloud/api) | Retrieve Quran verses, surahs and supported editions/translations. | Integration guide |
| API126 | [MP3Quran API](https://www.mp3quran.net/ar/api) | Find reciters, recitations and documented audio URLs. | Integration guide |

## Self-hosted software

| ID | Service & official setup | Purpose | NEXUS mode |
| --- | --- | --- | --- |
| API127 | [Ollama Local API](https://docs.ollama.com/api/introduction) | Run compatible language models locally and expose a local API. | Integration guide |
| API128 | [LibreTranslate Self-hosted](https://docs.libretranslate.com/) | Operate your own text-translation service using supported installed language models. | Integration guide |
| API129 | [PocketBase](https://pocketbase.io/docs/) | Build a lightweight backend with accounts, records, files and realtime updates. | Integration guide |
| API130 | [LocalAI](https://localai.io/) | Expose compatible AI inference APIs backed by models you operate. | Integration guide |
| API131 | [whisper.cpp Server](https://raw.githubusercontent.com/ggml-org/whisper.cpp/master/examples/server/README.md) | Transcribe speech using a local Whisper model and HTTP server. | Integration guide |
| API132 | [Kokoro-FastAPI](https://github.com/remsky/Kokoro-FastAPI) | Expose supported local text-to-speech generation through an API. | Integration guide |
| API133 | [ComfyUI Local Server](https://github.com/Comfy-Org/ComfyUI) | Execute local image/video workflows and connect them to an application. | Integration guide |
| API134 | [Qdrant Self-hosted](https://qdrant.tech/documentation/quickstart/) | Operate your own vector store for search and RAG. | Integration guide |
| API135 | [Chroma Self-hosted](https://docs.trychroma.com/docs/overview/introduction) | Store embeddings and retrieve relevant document chunks in a controlled environment. | Integration guide |
| API136 | [Meilisearch Self-hosted](https://www.meilisearch.com/docs/resources/self_hosting/getting_started/quick_start) | Provide typo-tolerant search and filters over application data. | Integration guide |
| API137 | [Typesense Self-hosted](https://typesense.org/docs/) | Build fast faceted search over product or document collections. | Integration guide |
| API138 | [Keycloak](https://www.keycloak.org/) | Operate identity, SSO and OAuth/OIDC services under your control. | Integration guide |
