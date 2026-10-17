# API activation reference — all 138 services

Research snapshot: 15 October 2026. Documentation packaged with NEXUS 0.6.19 on 17 October 2026. This is setup guidance; verify current vendor terms and rates. No accounts or credentials are included.

## API001 · Google Gemini API

**AI and LLMs · Chat connector**

Add text generation, summarization, structured extraction and multimodal understanding to an application.

[Official setup](https://aistudio.google.com/app/apikey)

**Credential:** Gemini API key associated with a Cloud project; current authorization keys can be service-account-bound.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Sign in to AI Studio, accept its terms, select or import the intended project, and obtain a restricted Gemini key.
3. Use the intended project key on the backend and validate model, quota, key restrictions and one test response.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Use the intended project key on the backend and validate model, quota, key restrictions and one test response.

**Monitoring:** Record model usage metadata and the project/model quota context. Multiple keys in the same project do not create independent free allowances.

**Caveat:** A free chat website and a paid consumer subscription are not API entitlements. Review free-tier data handling before sending private content.

[Reference 1](https://ai.google.dev/gemini-api/docs/api-key) · [Reference 2](https://ai.google.dev/gemini-api/docs/pricing) · [Reference 3](https://ai.google.dev/gemini-api/docs/rate-limits) · [Reference 4](https://ai.google.dev/gemini-api/docs/openai)

## API002 · Groq API

**AI and LLMs · Chat connector**

Run supported language models and speech recognition without hosting inference hardware.

[Official setup](https://console.groq.com/keys)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Groq organization key and select a model listed in your organization limits.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Capture usage tokens when returned, remaining requests (daily), remaining tokens (per minute), resets and Retry-After. These are not monetary balances.

**Caveat:** Requests and token budgets are shared at organization level. Preview models and audio products have separate limits.

[Reference 1](https://console.groq.com/docs/rate-limits) · [Reference 2](https://console.groq.com/docs/models) · [Reference 3](https://console.groq.com/docs/openai)

## API003 · OpenRouter Free

**AI and LLMs · Chat connector**

Access multiple model providers through one integration and evaluate free model routes.

[Official setup](https://openrouter.ai/settings/keys)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an OpenRouter key, set a key spending cap where useful, and explicitly select a verified free route.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** GET /api/v1/key documents key credit caps and usage. The rechecked schema does not document free_model_daily_requests; do not promise that counter. Missing values stay unknown.

**Caveat:** A free router may change models. A key spending limit is not the whole account balance. Do not assume a daily request counter exists in the key response.

[Reference 1](https://openrouter.ai/docs/api/api-reference/api-keys/get-current-api-key) · [Reference 2](https://openrouter.ai/docs/api_reference/limits) · [Reference 3](https://openrouter.ai/pricing) · [Reference 4](https://openrouter.ai/openrouter/free) · [Reference 5](https://openrouter.ai/pricing/)

## API004 · Mistral AI API

**AI and LLMs · Chat connector**

Add chat, coding, text analysis and supported document capabilities through a hosted API.

[Official setup](https://console.mistral.ai/api-keys)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a workspace API key and confirm Free mode, included usage, model availability and pay-as-you-go settings.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not treat old fixed-token or dollar allowances as a universal entitlement. Different capabilities consume different units.

[Reference 1](https://docs.mistral.ai/admin/billing-usage/usage-limits) · [Reference 2](https://docs.mistral.ai/api/endpoint/chat)

## API005 · Cloudflare Workers AI

**AI and LLMs · Integration guide**

Run eligible AI models close to your application using Workers bindings or REST.

[Official setup](https://dash.cloudflare.com/)

**Credential:** Scoped API token and account/resource ID, or a Workers binding; storage may use scoped S3 credentials.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Choose your Cloudflare account, create a scoped Workers AI token or binding, and select an eligible model.
3. Use the matching binding/REST/S3 protocol, restrict permissions, apply retention/caching rules and verify one operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Use the matching binding/REST/S3 protocol, restrict permissions, apply retention/caching rules and verify one operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Some models and features are outside the free allocation. Record model-specific consumption rather than assuming one request equals one Neuron.

[Reference 1](https://developers.cloudflare.com/workers-ai/platform/pricing/)

## API006 · OpenAI Moderation API

**AI and LLMs · Integration guide**

Classify potentially harmful text and image content as one component of application safety.

[Official setup](https://platform.openai.com/api-keys)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a project API key on the OpenAI API platform and restrict its use to the intended backend.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Count moderation attempts and outcomes separately from billed generation; do not equate a free moderation endpoint with unlimited throughput.

**Caveat:** Moderation is not chat, image generation or speech generation, and is not a guarantee that every harmful item will be detected.

[Reference 1](https://developers.openai.com/api/docs/guides/moderation) · [Reference 2](https://developers.openai.com/api/docs/models/omni-moderation-latest)

## API007 · Cohere Evaluation API

**AI and LLMs · Chat connector**

Evaluate language, retrieval and related AI capabilities before selecting a production plan.

[Official setup](https://docs.cohere.com/docs/rate-limits)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Cohere account and evaluation key; distinguish it from a production key before release.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not use evaluation availability as evidence of free commercial production access.

[Reference 1](https://docs.cohere.com/docs/rate-limits)

## API008 · Cerebras Inference

**AI and LLMs · Chat connector**

Evaluate hosted inference and compare its behavior with other model providers.

[Official setup](https://inference-docs.cerebras.ai/support/rate-limits)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create the account, review the trial conditions, and manually approve payment-method verification before API activation.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** The API remains inactive without required payment verification. Trial expiry is separate from rate limits.

[Reference 1](https://inference-docs.cerebras.ai/support/rate-limits)

## API009 · Hugging Face Inference Providers

**AI and LLMs · Chat connector**

Try multiple hosted model providers using a Hugging Face access token.

[Official setup](https://huggingface.co/settings/tokens)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Hugging Face token with inference permissions, review model gating, and use routed billing for included credits.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** This corrects earlier files that stated zero credits. Bring-your-own-provider-key billing is separate and does not use the same credit.

[Reference 1](https://huggingface.co/docs/inference-providers/en/pricing) · [Reference 2](https://huggingface.co/docs/inference-providers/pricing)

## API010 · Z.AI / Zhipu

**AI and LLMs · Integration guide**

Evaluate the specific Flash text or vision models that the relevant platform lists as free.

[Official setup](https://docs.z.ai/guides/overview/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Choose either the international Z.AI platform or the China platform, create the correct account/key, and check the model price.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** FlashX is not the same product as Flash. Regional platforms, keys, eligibility and retirements are not interchangeable.

[Reference 1](https://docs.z.ai/guides/overview/pricing) · [Reference 2](https://docs.z.ai/guides/overview/quick-start)

## API011 · Aion Labs

**AI and LLMs · Integration guide**

Evaluate supported text-generation models for a small prototype.

[Official setup](https://www.aionlabs.ai/docs/rate-limits/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a provider account/key and confirm that the selected model is included in the free account.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** The daily token ceiling can bind before the request ceiling. Confirm the balance and model eligibility in the account.

[Reference 1](https://www.aionlabs.ai/docs/rate-limits/) · [Reference 2](https://www.aionlabs.ai/pricing/)

## API012 · Kilo AI Gateway

**AI and LLMs · Integration guide**

Experiment with eligible free models through a gateway, including an anonymous access path.

[Official setup](https://kilo.ai/docs/gateway/authentication)

**Credential:** Anonymous requests only for eligible models; a provider token is required for account-backed access.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Select a currently free model and review anonymous gateway restrictions; create an account only for account features you need.
3. Select an eligible endpoint/model, implement per-IP backoff and do not forward confidential data without policy review.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Select an eligible endpoint/model, implement per-IP backoff and do not forward confidential data without policy review.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A public gateway is not an unlimited production entitlement. Do not send sensitive material without reviewing its data terms.

[Reference 1](https://kilo.ai/docs/gateway/authentication)

## API013 · LLM7.io

**AI and LLMs · Integration guide**

Try a limited hosted model gateway using its current token-based access.

[Official setup](https://docs.llm7.io/limits)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Obtain a current LLM7 API token and choose a model allowed by the token tier.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Older claims of unrestricted keyless access should not be reused. The provider states that free limits may be reduced.

[Reference 1](https://docs.llm7.io/limits) · [Reference 2](https://docs.llm7.io/quickstart) · [Reference 3](https://docs.llm7.io/guides/models-api)

## API014 · ModelScope

**AI and LLMs · Integration guide**

Investigate models exposed through ModelScope API-Inference.

[Official setup](https://www.modelscope.ai/docs/model-service/API-Inference/limits)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Review the official regional site, identity requirements, model entitlement and commercial-use terms before obtaining a token.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not copy a secondary directory's request count into a production quota. Real-name verification or regional restrictions may apply.

[Reference 1](https://www.modelscope.ai/docs/model-service/API-Inference/limits) · [Reference 2](https://modelscope.cn/docs/model-service/API-Inference/intro)

## API015 · NVIDIA NIM

**AI and LLMs · Chat connector**

Evaluate NVIDIA-hosted model endpoints and assess a later self-hosted NIM deployment.

[Official setup](https://docs.api.nvidia.com/nim/docs/product)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create the required developer account, complete the requested verification, accept model terms, and generate a key.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Free evaluation, self-hosting costs, model licenses and production licensing must be assessed separately.

[Reference 1](https://docs.api.nvidia.com/nim/docs/product)

## API016 · Ollama Cloud

**AI and LLMs · Integration guide**

Use hosted models when local hardware is insufficient.

[Official setup](https://docs.ollama.com/cloud)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create/sign in to an Ollama account, review its cloud plan, and obtain the cloud credentials required for your client.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A local client can route to cloud models. Local URL use alone does not establish local-only data processing.

[Reference 1](https://docs.ollama.com/cloud) · [Reference 2](https://docs.ollama.com/api/openai-compatibility)

## API017 · OVHcloud AI Endpoints

**AI and LLMs · Integration guide**

Evaluate hosted AI endpoints through anonymous testing or a provisioned cloud project.

[Official setup](https://docs.ovhcloud.com/en/guides/public-cloud/ai-machine-learning/ai-endpoints-getting-started)

**Credential:** Anonymous requests only for eligible models; a provider token is required for account-backed access.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Verify whether the desired model supports anonymous testing; use a project/key only after reviewing billing terms.
3. Select an eligible endpoint/model, implement per-IP backoff and do not forward confidential data without policy review.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Select an eligible endpoint/model, implement per-IP backoff and do not forward confidential data without policy review.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** An anonymous demo allowance is not the allowance of an authenticated account. No live regional test has been run.

[Reference 1](https://docs.ovhcloud.com/en/guides/public-cloud/ai-machine-learning/ai-endpoints-getting-started)

## API018 · SiliconFlow

**AI and LLMs · Integration guide**

Investigate hosted open-model inference on the platform available to your region.

[Official setup](https://docs.siliconflow.cn/cn/usercases/use-siliconcloud-in-ccswitch)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Choose the correct regional platform, complete required account or identity checks, create a key, and verify a zero-priced model.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A model appearing in /models does not prove that it is free. Registration and model licensing require confirmation.

[Reference 1](https://docs.siliconflow.cn/cn/usercases/use-siliconcloud-in-ccswitch) · [Reference 2](https://docs.siliconflow.cn/cn/legals/terms-of-service)

## API019 · OpenAI Generative API

**AI and LLMs · Chat connector**

Build text, image and audio features using paid API products and available account entitlements.

[Official setup](https://platform.openai.com/api-keys)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an API project, approve its billing or credit arrangement, create a restricted key, and set application-side limits.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Administrative keys can retrieve usage and costs by period. Keep them separate from runtime project keys. Reported cost does not by itself reveal prepaid credit balance.

**Caveat:** A ChatGPT login or subscription does not automatically activate paid API credits. Moderation is a separate no-cost endpoint.

[Reference 1](https://help.openai.com/en/articles/9039756-managing-billing-for-chatgpt-and-the-api-platform) · [Reference 2](https://developers.openai.com/api/docs/pricing) · [Reference 3](https://developers.openai.com/cookbook/examples/completions_usage_api)

## API020 · GitHub Models

**AI and LLMs · Integration guide**

Historical directory entry retained so old tutorials are not mistaken for an available integration.

[Official setup](https://docs.github.com/en/github-models)

**Credential:** Not applicable to new use.

1. Do not provision this retired service.
2. Select a supported replacement and migrate the integration.

**Implementation:** Remove retired endpoints from new configurations and migration plans.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** GitHub REST APIs and GitHub Copilot are separate products and are not described as retired here.

[Reference 1](https://docs.github.com/en/github-models)

## API021 · Azure AI Translator

**Translation, speech and OCR · Integration guide**

Translate application text, detect language and use supported dictionary or transliteration functions.

[Official setup](https://azure.microsoft.com/en-us/pricing/details/translator/)

**Credential:** Service key plus region/endpoint, or Microsoft Entra credentials where supported.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an Azure subscription/resource, explicitly choose the available F0 tier, and copy the region and resource credentials.
3. Use the resource-specific region and endpoint; test the chosen feature and verify its own character/audio quota.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Use the resource-specific region and endpoint; test the chosen feature and verify its own character/audio quota.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Document translation and specialized features may have different eligibility. Do not let provisioning silently choose a paid tier.

[Reference 1](https://azure.microsoft.com/en-us/pricing/details/translator/) · [Reference 2](https://www.microsoft.com/en-us/translator/business/faq/)

## API022 · Azure AI Speech

**Translation, speech and OCR · Integration guide**

Convert audio to text and text to neural speech for an application.

[Official setup](https://azure.microsoft.com/en-us/pricing/details/speech/)

**Credential:** Service key plus region/endpoint, or Microsoft Entra credentials where supported.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Speech resource in a supported region, select F0, and configure its SDK or REST credentials.
3. Use the resource-specific region and endpoint; test the chosen feature and verify its own character/audio quota.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Use the resource-specific region and endpoint; test the chosen feature and verify its own character/audio quota.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Audio seconds and synthesized characters are separate budgets. Batch, custom and premium features have different conditions.

[Reference 1](https://azure.microsoft.com/en-us/pricing/details/speech/)

## API023 · Google Cloud Text-to-Speech

**Translation, speech and OCR · Integration guide**

Generate speech from text for reading, accessibility and voice responses.

[Official setup](https://cloud.google.com/text-to-speech/pricing)

**Credential:** API key for supported products, or service account / OAuth / application-default credentials as documented.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Select a Cloud project, enable Text-to-Speech, approve billing, and configure a least-privilege runtime identity.
3. Configure the correct credential type, restrict keys where supported, separate projects/environments and test the exact product/SKU.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the correct credential type, restrict keys where supported, separate projects/environments and test the exact product/SKU.

**Monitoring:** Use project API metrics and relevant billing reports, with appropriate IAM. Keep SKU charges, request quota and user subscription allowances separate.

**Caveat:** The free allowance is voice/SKU-specific. Do not apply these counts to all Gemini or custom voice products.

[Reference 1](https://cloud.google.com/text-to-speech/pricing)

## API024 · Google Cloud Vision

**Translation, speech and OCR · Integration guide**

Extract printed text and detect supported visual features in images.

[Official setup](https://cloud.google.com/vision/pricing)

**Credential:** API key for supported products, or service account / OAuth / application-default credentials as documented.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Enable Vision in the intended billed project and configure a runtime identity with required permissions.
3. Configure the correct credential type, restrict keys where supported, separate projects/environments and test the exact product/SKU.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the correct credential type, restrict keys where supported, separate projects/environments and test the exact product/SKU.

**Monitoring:** Use project API metrics and relevant billing reports, with appropriate IAM. Keep SKU charges, request quota and user subscription allowances separate.

**Caveat:** One image with several requested features can create multiple billable units. Storage and other services may add charges.

[Reference 1](https://cloud.google.com/vision/pricing)

## API025 · Google Cloud Translation (NMT)

**Translation, speech and OCR · Integration guide**

Provide managed text translation inside a backend.

[Official setup](https://docs.cloud.google.com/translate/docs/setup)

**Credential:** API key for supported products, or service account / OAuth / application-default credentials as documented.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Enable Cloud Translation, link billing, choose Basic or Advanced, and use the authentication supported by that edition.
3. Configure the correct credential type, restrict keys where supported, separate projects/environments and test the exact product/SKU.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the correct credential type, restrict keys where supported, separate projects/environments and test the exact product/SKU.

**Monitoring:** Use project API metrics and relevant billing reports, with appropriate IAM. Keep SKU charges, request quota and user subscription allowances separate.

**Caveat:** The NMT allowance is not a blanket credit for document, custom-model or other translation products.

[Reference 1](https://docs.cloud.google.com/translate/docs/setup) · [Reference 2](https://cloud.google.com/products/translate/pricing)

## API026 · OCR.Space

**Translation, speech and OCR · Integration guide**

Convert supported image or PDF text into machine-readable output.

[Official setup](https://ocr.space/ocrapi)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Register for a free OCR key, select the engine, and enforce input-size and PDF-page limits before upload.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Earlier files contained inconsistent quota summaries. Do not treat 25,000/month as overriding an IP/day limit or page-size restriction.

[Reference 1](https://ocr.space/ocrapi) · [Reference 2](https://ocr.space/faq)

## API027 · ElevenLabs API Free

**Translation, speech and OCR · Integration guide**

Prototype supported speech generation and voice features.

[Official setup](https://elevenlabs.io/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an ElevenLabs account/key and check the free plan's voice, API and output-use entitlements.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** The earlier free-plan review excluded commercial use. Voice cloning also requires the speaker's authorization and applicable rights.

[Reference 1](https://elevenlabs.io/pricing) · [Reference 2](https://help.elevenlabs.io/hc/en-us/articles/13313564601361-Can-I-publish-the-content-I-generate-on-the-platform)

## API028 · DeepL API Free / Developer

**Translation, speech and OCR · Integration guide**

Evaluate text translation through an API, while separating legacy and new account plans.

[Official setup](https://support.deepl.com/hc/en-us/articles/360021200939-DeepL-API-plans)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Inspect the plan offered to your account, select an API plan rather than a web-translator plan, and create a key.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** The earlier claim that every new account gets 500,000 free characters/month was incorrect. Check checkout pricing and eligibility before subscribing.

[Reference 1](https://support.deepl.com/hc/en-us/articles/360021200939-DeepL-API-plans) · [Reference 2](https://developers.deepl.com/docs/resources/usage-limits)

## API029 · MyMemory

**Translation, speech and OCR · Integration guide**

Add lightweight translation to small applications or prototypes.

[Official setup](https://mymemory.translated.net/doc/usagelimits.php)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Read the usage policy and set an appropriate contact identifier only when needed for the higher documented limit.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Not a substitute for a private translation contract. Review how submitted text is used and avoid exposing personal content unnecessarily.

[Reference 1](https://mymemory.translated.net/doc/usagelimits.php) · [Reference 2](https://mymemory.translated.net/doc/spec.php)

## API030 · Deepgram

**Translation, speech and OCR · Integration guide**

Evaluate speech recognition and other supported speech APIs.

[Official setup](https://deepgram.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create the account, inspect the exact trial balance and expiry, and generate a scoped project key.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Track seconds and feature charges. A trial offer does not establish indefinite free speech processing.

[Reference 1](https://deepgram.com/pricing)

## API031 · Brave Search API

**Web search and extraction · Integration guide**

Add search results to an application or AI research workflow.

[Official setup](https://brave.com/search/api/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Search API subscription/key, review card requirements, and select the correct search product.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Credit-to-request conversion changes with product and price. Search licensing and downstream use still apply.

[Reference 1](https://brave.com/search/api/)

## API032 · Tavily API

**Web search and extraction · Integration guide**

Retrieve web results and evidence for AI-assisted research.

[Official setup](https://www.tavily.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Tavily account/key and set the intended search depth and credit budget.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** One application question can invoke several searches. Do not count one search credit as one complete user task.

[Reference 1](https://www.tavily.com/pricing)

## API033 · Exa API

**Web search and extraction · Integration guide**

Find semantically relevant pages and retrieve their content.

[Official setup](https://exa.ai/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an Exa key and select search/content operations after checking their separate unit prices.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** More results, content extraction and advanced search modes can change the cost of a query.

[Reference 1](https://exa.ai/pricing)

## API034 · Firecrawl API

**Web search and extraction · Integration guide**

Extract web pages as Markdown or structured data for indexing and retrieval.

[Official setup](https://www.firecrawl.dev/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a key, choose a scrape or search operation, and restrict crawl scope and concurrency.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A site crawl can multiply calls rapidly. Respect source-site access restrictions, robots policies and content rights.

[Reference 1](https://www.firecrawl.dev/pricing)

## API035 · Jina Reader API

**Web search and extraction · Integration guide**

Convert a URL into readable content for an AI or search pipeline.

[Official setup](https://jina.ai/reader/)

**Credential:** No secret on the public path; optional provider token or application identification where documented.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Test the public reader within documented limits; create a Jina key only for the authenticated entitlement you need.
3. Use one explicit access path; do not mix anonymous and authenticated quota assumptions.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Use one explicit access path; do not mix anonymous and authenticated quota assumptions.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not call a one-time token grant a monthly allowance. Retrieved pages remain untrusted content, not executable instructions.

[Reference 1](https://jina.ai/reader/)

## API036 · SerpApi

**Web search and extraction · Integration guide**

Receive search-engine results as structured JSON.

[Official setup](https://serpapi.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a SerpApi key and choose the supported engine and request parameters.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** It is a third-party search-results provider, not the official Google Search API. Check downstream rights and query accounting.

[Reference 1](https://serpapi.com/pricing)

## API037 · Supabase

**Databases and backend · Integration guide**

Build a PostgreSQL-backed app with authentication, storage, REST access and realtime features.

[Official setup](https://supabase.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an organization/project, choose a region, define the schema, and configure row-level security before exposing client access.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Publishable/anonymous client keys are not service-role secrets. Free-project inactivity and backup limits require a separate operating plan.

[Reference 1](https://supabase.com/pricing)

## API038 · Firebase / Cloud Firestore

**Databases and backend · Integration guide**

Store application documents with SDK synchronization and controlled client access.

[Official setup](https://firebase.google.com/pricing)

**Credential:** Firebase app configuration plus appropriate SDK identity, security rules and/or server service-account authorization.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Firebase project, register the app, create the Firestore database, choose its region and deploy restrictive Security Rules.
3. Install the platform SDK, configure secure rules or server permissions, register device/app details and perform a controlled feature test.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install the platform SDK, configure secure rules or server permissions, register device/app details and perform a controlled feature test.

**Monitoring:** Use project API metrics and relevant billing reports, with appropriate IAM. Keep SKU charges, request quota and user subscription allowances separate.

**Caveat:** Creating a Firebase project does not create every database or authorize all users. Test rules and indexes before launch.

[Reference 1](https://firebase.google.com/pricing)

## API039 · Neon Postgres

**Databases and backend · Integration guide**

Run managed PostgreSQL without administering a database VM.

[Official setup](https://neon.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a project/database and a least-privilege database role, then store the TLS connection string on the backend.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** This is not automatically a public REST CRUD backend. Protect connection strings and account for autosuspend and resource limits.

[Reference 1](https://neon.com/pricing)

## API040 · Upstash Redis REST

**Databases and backend · Integration guide**

Add caching, counters, sessions and application rate limits.

[Official setup](https://upstash.com/pricing/redis)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create the eligible Redis database and obtain its scoped REST token or Redis credentials.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A single logical operation may use multiple commands. Do not put full-access database credentials in a public client.

[Reference 1](https://upstash.com/pricing/redis) · [Reference 2](https://upstash.com/docs/redis/overall/billing) · [Reference 3](https://upstash.com/blog/redis-pricing-comparison-every-major-provider-in-2026-with-numbers)

## API041 · Appwrite Cloud

**Databases and backend · Integration guide**

Use managed accounts, databases, file storage, functions and realtime services.

[Official setup](https://appwrite.io/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a project, register allowed app platforms, define data permissions and generate only the required server API key scopes.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Project creation is not equivalent to application configuration. Verify each Free-plan resource limit in the console.

[Reference 1](https://appwrite.io/pricing) · [Reference 2](https://appwrite.io/docs/advanced/billing/free)

## API042 · Qdrant Cloud

**Databases and backend · Integration guide**

Store embeddings for semantic search and retrieval-augmented generation.

[Official setup](https://qdrant.tech/pricing/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create the free cluster, copy its endpoint/key and create collections with the correct vector dimensions.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Model embedding costs are separate. A small free cluster is not a high-availability production guarantee.

[Reference 1](https://qdrant.tech/pricing/)

## API043 · Pinecone Starter

**Databases and backend · Integration guide**

Host vector or hybrid search indexes for retrieval and recommendations.

[Official setup](https://www.pinecone.io/pricing/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Starter project/key and an index matched to your embedding model and region.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not confuse Starter with a time-limited paid-plan trial. Inference, storage and query accounting are distinct.

[Reference 1](https://www.pinecone.io/pricing/)

## API044 · Cloudflare D1

**Databases and backend · Integration guide**

Store SQL data for a Workers-based backend.

[Official setup](https://developers.cloudflare.com/d1/platform/pricing/)

**Credential:** Scoped API token and account/resource ID, or a Workers binding; storage may use scoped S3 credentials.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create the database, apply migrations and bind it to the intended Worker or scoped API token.
3. Use the matching binding/REST/S3 protocol, restrict permissions, apply retention/caching rules and verify one operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Use the matching binding/REST/S3 protocol, restrict permissions, apply retention/caching rules and verify one operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Usage counts rows, not merely SQL statements. An inefficient scan can consume a large read allowance.

[Reference 1](https://developers.cloudflare.com/d1/platform/pricing/)

## API045 · Turso

**Databases and backend · Integration guide**

Use managed SQLite/libSQL databases for lightweight distributed applications.

[Official setup](https://turso.tech/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a database and restricted database token, then configure the client with its database URL.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Protect tokens and distinguish database count from read, write and storage entitlements.

[Reference 1](https://turso.tech/pricing)

## API046 · Cloudflare Workers KV

**Databases and backend · Integration guide**

Store configuration, cached values and simple key-value data at the edge.

[Official setup](https://developers.cloudflare.com/kv/platform/pricing/)

**Credential:** Scoped API token and account/resource ID, or a Workers binding; storage may use scoped S3 credentials.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a KV namespace, bind it to a Worker and select only the needed token permissions.
3. Use the matching binding/REST/S3 protocol, restrict permissions, apply retention/caching rules and verify one operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Use the matching binding/REST/S3 protocol, restrict permissions, apply retention/caching rules and verify one operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Choose data consistency requirements deliberately; do not use a cache-shaped service as an unexamined financial ledger.

[Reference 1](https://developers.cloudflare.com/kv/platform/pricing/)

## API047 · Cloudflare Workers

**Databases and backend · Integration guide**

Deploy HTTP endpoints, backend logic and edge request processing.

[Official setup](https://developers.cloudflare.com/workers/platform/pricing/)

**Credential:** Scoped API token and account/resource ID, or a Workers binding; storage may use scoped S3 credentials.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Worker, configure secrets/bindings and routes, then deploy an authenticated endpoint where required.
3. Use the matching binding/REST/S3 protocol, restrict permissions, apply retention/caching rules and verify one operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Use the matching binding/REST/S3 protocol, restrict permissions, apply retention/caching rules and verify one operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Request count is only one constraint. Connected storage, paid APIs and model inference have their own charges.

[Reference 1](https://developers.cloudflare.com/workers/platform/pricing/)

## API048 · Firebase Authentication

**Identity and security · Integration guide**

Manage application users and supported sign-in providers.

[Official setup](https://firebase.google.com/pricing)

**Credential:** Firebase app configuration plus appropriate SDK identity, security rules and/or server service-account authorization.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Register the app and explicitly enable each sign-in provider, allowed domain and required client credential.
3. Install the platform SDK, configure secure rules or server permissions, register device/app details and perform a controlled feature test.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install the platform SDK, configure secure rules or server permissions, register device/app details and perform a controlled feature test.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Google sign-in for your app requires its own configuration. It does not authorize Gmail, Drive or every Google Cloud API.

[Reference 1](https://firebase.google.com/pricing) · [Reference 2](https://firebase.google.com/docs/auth/web/google-signin)

## API049 · Clerk

**Identity and security · Integration guide**

Add user sessions, hosted sign-in screens and account management.

[Official setup](https://clerk.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an application, select sign-in methods, configure origins/redirects and separate public from secret keys.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** SSO with Google is a sign-in option only when configured. It does not grant permission to Google user content.

[Reference 1](https://clerk.com/pricing)

## API050 · Auth0

**Identity and security · Integration guide**

Provide OAuth/OIDC login, identity federation and token-based application access.

[Official setup](https://auth0.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a tenant and application, configure callback/logout URLs, APIs, audiences and approved identity connections.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Identity authentication and resource authorization are different. Management tokens must remain on trusted servers.

[Reference 1](https://auth0.com/pricing)

## API051 · Cloudflare Turnstile

**Identity and security · Integration guide**

Reduce automated abuse of forms, login and account creation.

[Official setup](https://developers.cloudflare.com/turnstile/plans/)

**Credential:** Public sitekey on the frontend; secret key on the backend.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a widget for the permitted domains, install its site key and keep its verification secret server-side.
3. Render the widget and verify tokens server-side with expiry and failure handling.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Render the widget and verify tokens server-side with expiry and failure handling.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Rendering the widget is insufficient: validate each returned token on the backend and do not treat it as user authentication.

[Reference 1](https://developers.cloudflare.com/turnstile/plans/) · [Reference 2](https://developers.cloudflare.com/turnstile/get-started/)

## API052 · HIBP Pwned Passwords

**Identity and security · Integration guide**

Check whether a password hash prefix appears in the breach corpus.

[Official setup](https://haveibeenpwned.com/API/V3)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Implement the hash-prefix range lookup and compare suffixes locally; never submit the plaintext password.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not log passwords or full unsalted password hashes. This is a password-screening signal, not a complete security assessment.

[Reference 1](https://haveibeenpwned.com/API/V3) · [Reference 2](https://haveibeenpwned.com/API/v3)

## API053 · Resend

**Email, notifications and realtime · Integration guide**

Send transactional email such as verification messages and receipts.

[Official setup](https://resend.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an API key, verify a sending domain and publish the required DNS records before using production recipients.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Trial/test sender permissions may restrict recipients. Delivery, bounces and suppression handling require backend work.

[Reference 1](https://resend.com/pricing)

## API054 · Mailjet

**Email, notifications and realtime · Integration guide**

Send application email through an API or SMTP.

[Official setup](https://www.mailjet.com/pricing/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create API credentials, verify the sender/domain and configure SPF/DKIM as instructed.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Daily and monthly limits apply together. Do not confuse email verification codes with free SMS delivery.

[Reference 1](https://www.mailjet.com/pricing/)

## API055 · Firebase Cloud Messaging

**Email, notifications and realtime · Integration guide**

Deliver push notifications to registered Android, iOS and web app instances.

[Official setup](https://firebase.google.com/pricing)

**Credential:** Firebase app configuration plus appropriate SDK identity, security rules and/or server service-account authorization.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Register each app, obtain device tokens, configure server credentials and notification permissions; add APNs/web configuration where needed.
3. Install the platform SDK, configure secure rules or server permissions, register device/app details and perform a controlled feature test.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install the platform SDK, configure secure rules or server permissions, register device/app details and perform a controlled feature test.

**Monitoring:** Record sends and provider message IDs. API acceptance does not prove device display. No universal cash balance is implied by message counts.

**Caveat:** Device tokens are delivery addresses, not account passwords. Push does not automatically implement incoming calls or SMS.

[Reference 1](https://firebase.google.com/pricing) · [Reference 2](https://firebase.google.com/docs/cloud-messaging) · [Reference 3](https://firebase.google.com/docs/cloud-messaging/send/v1-api)

## API056 · Telegram Bot API

**Email, notifications and realtime · Integration guide**

Build bot commands, customer-service interactions and operational notifications inside Telegram.

[Official setup](https://core.telegram.org/bots/faq)

**Credential:** Bot token; user/chat identifiers and optional webhook secret.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a bot through BotFather, store its token, and configure polling or an HTTPS webhook.
3. Protect the token, validate webhooks, record chat authorization and respect message/broadcast limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Protect the token, validate webhooks, record chat authorization and respect message/broadcast limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A bot normally cannot initiate a private conversation before the person interacts with it. Treat webhook and bot credentials as secrets.

[Reference 1](https://core.telegram.org/bots/faq)

## API057 · Discord API / Webhooks

**Email, notifications and realtime · Integration guide**

Send team alerts or build community bot integrations.

[Official setup](https://docs.discord.com/developers/resources/webhook)

**Credential:** Webhook URL/token for the destination; bot applications use separate credentials.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create the bot or channel webhook with the required server permissions and store its token or webhook URL privately.
3. Keep webhook URLs server-side, validate payloads and implement retry-after/backoff.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Keep webhook URLs server-side, validate payloads and implement retry-after/backoff.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A webhook URL can grant posting access. Respect Retry-After and limit bot permissions to the intended channels.

[Reference 1](https://docs.discord.com/developers/resources/webhook) · [Reference 2](https://docs.discord.com/developers/topics/rate-limits)

## API058 · Pusher Channels

**Email, notifications and realtime · Integration guide**

Publish live chat events, presence and interface updates.

[Official setup](https://pusher.com/channels/pricing/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Channels application and implement server authentication for private/presence channels.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Connections and messages are different limits. Realtime transport alone does not provide chat storage or user authorization.

[Reference 1](https://pusher.com/channels/pricing/)

## API059 · Ably

**Email, notifications and realtime · Integration guide**

Synchronize application events, chat and presence over managed realtime channels.

[Official setup](https://ably.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an application/key and issue restricted short-lived client tokens from your backend.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Check channel, connection and message accounting. Do not place an unrestricted root key in a mobile application.

[Reference 1](https://ably.com/pricing)

## API060 · OneSignal

**Email, notifications and realtime · Integration guide**

Manage push delivery and targeted messaging across supported channels.

[Official setup](https://onesignal.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an application, configure each platform's push credentials, install the SDK and collect appropriate consent.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A provider dashboard does not override iOS/Android permission or background-execution requirements.

[Reference 1](https://onesignal.com/pricing)

## API061 · Brevo Email API

**Email, notifications and realtime · Integration guide**

Send verification, order and other transactional emails.

[Official setup](https://www.brevo.com/features/email-api/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create the account/API key, validate sender/domain ownership and configure required authentication records.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Free email is not a free SMS product. Review sender restrictions and contact-data responsibilities.

[Reference 1](https://www.brevo.com/features/email-api/) · [Reference 2](https://help.brevo.com/hc/en-us/articles/208580669-FAQs-What-are-the-limits-of-the-Free-plan)

## API062 · Daily Video API

**Email, notifications and realtime · Integration guide**

Embed voice/video rooms and participant sessions in an app.

[Official setup](https://www.daily.co/pricing/video-sdk/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an account/key, configure private rooms and issue meeting tokens from the backend.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** One two-person minute equals two participant-minutes. Recording, streaming and other features can have separate prices.

[Reference 1](https://www.daily.co/pricing/video-sdk/)

## API063 · Twilio SMS / Voice

**Email, notifications and realtime · Integration guide**

Evaluate SMS verification, messaging or programmable voice.

[Official setup](https://www.twilio.com/docs/usage/tutorials/how-to-use-your-free-trial-account)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create and verify an account, review allowed destination countries, verify required recipients and configure a test sender.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Egypt SMS delivery is not established here. Trial credits and test credentials are not permission to impersonate senders.

[Reference 1](https://www.twilio.com/docs/usage/tutorials/how-to-use-your-free-trial-account)

## API064 · Cloudflare R2

**Storage and media · Integration guide**

Store files and objects using an S3-compatible interface.

[Official setup](https://developers.cloudflare.com/r2/pricing/)

**Credential:** Scoped API token and account/resource ID, or a Workers binding; storage may use scoped S3 credentials.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Activate R2 under the approved account, review its billing enrollment, create a bucket and scoped S3 credentials.
3. Use the matching binding/REST/S3 protocol, restrict permissions, apply retention/caching rules and verify one operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Use the matching binding/REST/S3 protocol, restrict permissions, apply retention/caching rules and verify one operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Free storage does not make all operations or storage classes free. Bucket privacy and signed access need explicit configuration.

[Reference 1](https://developers.cloudflare.com/r2/pricing/)

## API065 · Firebase Cloud Storage

**Storage and media · Integration guide**

Store user uploads and application media with Firebase access controls.

[Official setup](https://firebase.google.com/docs/storage/faqs-storage-changes-announced-sept-2024)

**Credential:** Firebase app configuration plus appropriate SDK identity, security rules and/or server service-account authorization.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Approve Blaze billing, create/select the bucket and region, and deploy restrictive storage rules.
3. Install the platform SDK, configure secure rules or server permissions, register device/app details and perform a controlled feature test.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install the platform SDK, configure secure rules or server permissions, register device/app details and perform a controlled feature test.

**Monitoring:** Use project API metrics and relevant billing reports, with appropriate IAM. Keep SKU charges, request quota and user subscription allowances separate.

**Caveat:** Signing into Firebase does not bypass billing. Existing Spark projects can receive 402/403 for bucket access.

[Reference 1](https://firebase.google.com/docs/storage/faqs-storage-changes-announced-sept-2024)

## API066 · Cloudinary

**Storage and media · Integration guide**

Upload, transform, optimize and deliver images or video.

[Official setup](https://cloudinary.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a product environment, configure signed uploads and transformations, and keep the API secret server-side.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A credit is a shared resource unit, not one image or one API call. Avoid unrestricted upload presets.

[Reference 1](https://cloudinary.com/pricing)

## API067 · ImageKit

**Storage and media · Integration guide**

Optimize media and provide responsive image/video delivery.

[Official setup](https://imagekit.io/plans/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an account, configure origin/media library and signed uploads, and separate public from private keys.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Storage, delivery bandwidth and transformations are distinct. Public delivery URLs do not require exposing a private API key.

[Reference 1](https://imagekit.io/plans/)

## API068 · Unsplash API

**Storage and media · Integration guide**

Search and display photographic images with creator metadata.

[Official setup](https://unsplash.com/documentation)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Register an application, obtain an access key, implement attribution/download tracking and request production approval if needed.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Follow hotlinking and attribution rules. API access does not remove the conditions attached to the content.

[Reference 1](https://unsplash.com/documentation)

## API069 · Pixabay API

**Storage and media · Integration guide**

Search supported images, illustrations and videos.

[Official setup](https://pixabay.com/api/docs/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Register for an API key and implement query caching and the required image/video usage conditions.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Avoid bulk mirroring and redistributing a competing library. Review each content type and licensing restriction.

[Reference 1](https://pixabay.com/api/docs/)

## API070 · Openverse API

**Storage and media · Integration guide**

Discover images and audio with open-license metadata.

[Official setup](https://docs.openverse.org/api/reference/authentication_and_throttling.html)

**Credential:** No secret on the public path; optional provider token or application identification where documented.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Choose anonymous access or register an OAuth client for higher limits, and preserve each result's license/attribution.
3. Use one explicit access path; do not mix anonymous and authenticated quota assumptions.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Use one explicit access path; do not mix anonymous and authenticated quota assumptions.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** An open-search result is not automatically cleared for all commercial uses. Inspect the individual license and source.

[Reference 1](https://docs.openverse.org/api/reference/authentication_and_throttling.html)

## API071 · Pexels API

**Storage and media · Integration guide**

Search photo and video assets for supported application experiences.

[Official setup](https://www.pexels.com/api/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Use the API registration flow, describe the application, obtain the key if approved and implement attribution.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Actual account issuance was not tested. The API must not be used to copy the core Pexels library or unsupported wallpaper-app functionality.

[Reference 1](https://www.pexels.com/api/) · [Reference 2](https://www.pexels.com/onboarding/) · [Reference 3](https://www.pexels.com/api/documentation/)

## API072 · Geoapify

**Maps and geolocation · Integration guide**

Add geocoding, routes, places and mapping functions.

[Official setup](https://www.geoapify.com/pricing/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a project/API key, select the needed APIs and configure key restrictions and attribution.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Credits are not identical to requests across every operation. Verify commercial and attribution terms for your exact use.

[Reference 1](https://www.geoapify.com/pricing/)

## API073 · LocationIQ

**Maps and geolocation · Integration guide**

Convert addresses to coordinates and coordinates to addresses.

[Official setup](https://locationiq.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an access token, restrict allowed use and include the required attribution for eligible free commercial use.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Check commercial eligibility and caching rights. Address services are not a complete ride-dispatch backend.

[Reference 1](https://locationiq.com/pricing)

## API074 · Nominatim - OSM public server

**Maps and geolocation · Integration guide**

Perform low-volume address search against OpenStreetMap data.

[Official setup](https://operations.osmfoundation.org/policies/nominatim/)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Set an identifying User-Agent/contact, use caching and throttle centrally to the service policy.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not use the public server for mass geocoding or client-side autocomplete. Open data does not imply unlimited hosted infrastructure.

[Reference 1](https://operations.osmfoundation.org/policies/nominatim/)

## API075 · TomTom Maps APIs

**Maps and geolocation · Integration guide**

Use maps, routing, geocoding and traffic data.

[Official setup](https://docs.tomtom.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a developer application/key and select the routing, mapping or geocoding product required.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Separate tile requests from route and search requests. Region coverage and data permissions need product-level review.

[Reference 1](https://docs.tomtom.com/pricing)

## API076 · Google Maps Platform

**Maps and geolocation · Integration guide**

Add maps, routes, places and distance-related functions to an application.

[Official setup](https://developers.google.com/maps/billing-and-pricing/pricing)

**Credential:** API key for supported products, or service account / OAuth / application-default credentials as documented.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create/select a project, enable only the specific Maps APIs, approve billing and restrict keys by API and app/server.
3. Configure the correct credential type, restrict keys where supported, separate projects/environments and test the exact product/SKU.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the correct credential type, restrict keys where supported, separate projects/environments and test the exact product/SKU.

**Monitoring:** Use project API metrics and relevant billing reports, with appropriate IAM. Keep SKU charges, request quota and user subscription allowances separate.

**Caveat:** One Google account does not enable Maps automatically. Attribution, caching and billing rules vary by service.

[Reference 1](https://developers.google.com/maps/billing-and-pricing/pricing) · [Reference 2](https://mapsplatform.google.com/pricing/)

## API077 · Mapbox APIs

**Maps and geolocation · Integration guide**

Build styled maps, search and navigation experiences.

[Official setup](https://www.mapbox.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create the account/token, select SDKs or APIs, and restrict scopes and allowed URLs where supported.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not apply a map-display allowance to Directions, Search or Navigation. Tokens need appropriate restrictions.

[Reference 1](https://www.mapbox.com/pricing)

## API078 · GeoNames

**Maps and geolocation · Integration guide**

Look up place names and geographic reference data.

[Official setup](https://www.geonames.org/export/web-services.html)

**Credential:** Registered username; not necessarily a secret bearer token.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Register a GeoNames username and enable free web-service access in account settings.
3. Pass the correct username, cache results and monitor the shared account credit limit.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Pass the correct username, cache results and monitor the shared account credit limit.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A username is not a private bearer secret, but usage still belongs to your account and can be exhausted.

[Reference 1](https://www.geonames.org/export/web-services.html)

## API079 · IPinfo Lite

**Maps and geolocation · Integration guide**

Enrich an IP address with basic network/country information.

[Official setup](https://ipinfo.io/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Lite account/token and use only the endpoint and fields included in that plan.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** IP geolocation is approximate and is not phone GPS. Do not assume premium fields are part of Lite.

[Reference 1](https://ipinfo.io/pricing)

## API080 · REST Countries

**Maps and geolocation · Integration guide**

Retrieve country names, codes, languages, currencies and related reference fields.

[Official setup](https://restcountries.com/plans)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Confirm the current API version and plan, create the required key, and cache slowly changing country data.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not hardcode an obsolete unauthenticated route into a new project without testing it.

[Reference 1](https://restcountries.com/plans) · [Reference 2](https://restcountries.com/docs/countries/api-versions) · [Reference 3](https://restcountries.com/docs/countries)

## API081 · ipify

**Maps and geolocation · Integration guide**

Return the public IPv4/IPv6 address visible to the service.

[Official setup](https://www.ipify.org/)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Choose the IPv4 or IPv6 endpoint and parse its text or JSON response.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** The reported IP may be a NAT, proxy or VPN egress address. It is not the user's precise location.

[Reference 1](https://www.ipify.org/)

## API082 · OpenCage Free Trial

**Maps and geolocation · Integration guide**

Evaluate forward and reverse geocoding.

[Official setup](https://opencagedata.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a trial account/key and review production licensing before publishing the feature.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Daily trial headroom does not imply permission to run a commercial app indefinitely without a paid plan.

[Reference 1](https://opencagedata.com/pricing)

## API083 · Open-Meteo

**Weather and environment · Integration guide**

Retrieve weather forecasts and supported historical or environmental datasets.

[Official setup](https://open-meteo.com/en/pricing)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Select the variables and location, read the hosted-use policy, and cache requests appropriately.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** The software/data licensing and the free hosted-service conditions are distinct. A commercial app needs the appropriate access path.

[Reference 1](https://open-meteo.com/en/pricing)

## API084 · OpenWeather

**Weather and environment · Integration guide**

Display current conditions and selected forecast products.

[Official setup](https://openweathermap.org/price)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create the account/key, activate the intended product and confirm whether its plan requires separate billing.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A key may need provider-side activation. One Call and standard weather endpoints do not share identical pricing.

[Reference 1](https://openweathermap.org/price)

## API085 · WeatherAPI.com

**Weather and environment · Integration guide**

Add weather, forecasts and related location data to an application.

[Official setup](https://www.weatherapi.com/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Register for a free key and choose fields and forecast days available in the plan.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Historical data and longer forecasts can require another plan. Verify the commercial-use conditions before release.

[Reference 1](https://www.weatherapi.com/) · [Reference 2](https://www.weatherapi.com/pricing.aspx)

## API086 · OpenAQ API v3

**Weather and environment · Integration guide**

Read air-quality observations and station metadata.

[Official setup](https://docs.openaq.org/using-the-api/api-key)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create an OpenAQ key and use the v3 endpoints, filters and pagination.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Station coverage and reporting delay vary. Data is not a substitute for a guaranteed personal exposure measurement.

[Reference 1](https://docs.openaq.org/using-the-api/api-key)

## API087 · Tomorrow.io

**Weather and environment · Integration guide**

Add weather conditions and forecasts to location-aware applications.

[Official setup](https://support.tomorrow.io/hc/en-us/articles/20273728362644-Free-API-Plan-Rate-Limits)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a free key and choose the weather fields allowed by the plan.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** The hourly limit can bind before the daily allowance. Premium datasets may not be included.

[Reference 1](https://support.tomorrow.io/hc/en-us/articles/20273728362644-Free-API-Plan-Rate-Limits)

## API088 · Frankfurter API

**Currencies and finance data · Integration guide**

Convert reference currency values and retrieve historical rates.

[Official setup](https://frankfurter.dev/)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Choose the base/quote currencies and date, validate supported currencies and cache daily values.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Reference rates are not live executable trading prices or the rate of every Egyptian bank.

[Reference 1](https://frankfurter.dev/)

## API089 · ExchangeRate-API Open

**Currencies and finance data · Integration guide**

Use periodically updated currency conversion tables.

[Official setup](https://www.exchangerate-api.com/docs/free)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Use the Open Access endpoint, cache daily data and show the required attribution.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not redistribute the source dataset contrary to its terms. Daily rates are not transaction quotes.

[Reference 1](https://www.exchangerate-api.com/docs/free)

## API090 · CoinGecko Demo API

**Currencies and finance data · Integration guide**

Read cryptocurrency prices and market metadata for a prototype.

[Official setup](https://www.coingecko.com/en/api/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Demo key, use the Demo endpoint/header and comply with attribution/license conditions.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Freshness, redistribution and commercial data licensing require review. This is data access, not investment advice or exchange execution.

[Reference 1](https://www.coingecko.com/en/api/pricing)

## API091 · Alpha Vantage

**Currencies and finance data · Integration guide**

Retrieve selected market time series and technical indicator data.

[Official setup](https://www.alphavantage.co/support/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Request a free key and choose an endpoint and market dataset actually included in the plan.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Real-time, premium and licensed exchange data can be excluded. A free key does not unlock every endpoint.

[Reference 1](https://www.alphavantage.co/support/)

## API092 · Twelve Data Basic

**Currencies and finance data · Integration guide**

Prototype financial market data queries and indicators.

[Official setup](https://twelvedata.com/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Basic key, inspect the credits consumed by each operation and check display/commercial rights.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not assume a free development plan permits redistribution or a customer-facing real-time market feed.

[Reference 1](https://twelvedata.com/pricing)

## API093 · Stripe Sandbox

**Currencies and finance data · Integration guide**

Test payment flows, webhooks and failure handling without moving real money.

[Official setup](https://docs.stripe.com/sandboxes)

**Credential:** Sandbox/test keys and test webhook signing secrets.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a sandbox, use test keys/cards and verify webhook signatures; separate all test and live configurations.
3. Keep test/live keys and webhooks separate; use synthetic test data, not real payment details.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Keep test/live keys and webhooks separate; use synthetic test data, not real payment details.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Successful simulation does not prove live merchant eligibility in Egypt or another jurisdiction. Never present test payments as settled funds.

[Reference 1](https://docs.stripe.com/sandboxes)

## API094 · GitHub REST API

**Developer and workspace integrations · Integration guide**

Read repository metadata and automate issues, pull requests and releases with appropriate permissions.

[Official setup](https://docs.github.com/en/rest/using-the-rest-api/rate-limits-for-the-rest-api)

**Credential:** No secret on the public path; optional provider token or application identification where documented.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Use public read access where sufficient; otherwise create a fine-grained token or GitHub App restricted to the required repositories.
3. Use one explicit access path; do not mix anonymous and authenticated quota assumptions.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Use one explicit access path; do not mix anonymous and authenticated quota assumptions.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Reading public repositories is different from write authorization. GitHub Models retirement does not retire this API.

[Reference 1](https://docs.github.com/en/rest/using-the-rest-api/rate-limits-for-the-rest-api)

## API095 · Google Sheets API

**Developer and workspace integrations · Integration guide**

Read/write spreadsheet data and automate reports with owner-authorized access.

[Official setup](https://console.cloud.google.com/apis/library/sheets.googleapis.com)

**Credential:** OAuth client ID/configuration and short-lived access tokens; refresh tokens kept securely. Service accounts only with explicitly granted access or valid admin delegation.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Enable Sheets, configure an OAuth client and scopes, then obtain consent; alternatively share only designated files with an authorized service account.
3. Implement OAuth redirects/state/PKCE as appropriate, least-privilege scopes, secure token storage, revocation and consent error handling.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement OAuth redirects/state/PKCE as appropriate, least-privilege scopes, secure token storage, revocation and consent error handling.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A Google login does not grant access to every spreadsheet. Enabling the API and granting access to a particular file are separate steps.

[Reference 1](https://developers.google.com/workspace/sheets/api/quickstart/python) · [Reference 2](https://developers.google.com/workspace/sheets/api/limits)

## API096 · Google Docs API

**Developer and workspace integrations · Integration guide**

Create and modify native documents programmatically.

[Official setup](https://console.cloud.google.com/apis/library/docs.googleapis.com)

**Credential:** OAuth client ID/configuration and short-lived access tokens; refresh tokens kept securely. Service accounts only with explicitly granted access or valid admin delegation.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Enable Docs, configure the OAuth app and minimum scopes, and obtain access to the intended document.
3. Implement OAuth redirects/state/PKCE as appropriate, least-privilege scopes, secure token storage, revocation and consent error handling.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement OAuth redirects/state/PKCE as appropriate, least-privilege scopes, secure token storage, revocation and consent error handling.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Creating a credential does not automatically grant permission to existing user documents.

[Reference 1](https://developers.google.com/workspace/docs/api/limits)

## API097 · Google Drive API

**Developer and workspace integrations · Integration guide**

List, upload, organize and share files under an authorized identity.

[Official setup](https://console.cloud.google.com/apis/library/drive.googleapis.com)

**Credential:** OAuth client ID/configuration and short-lived access tokens; refresh tokens kept securely. Service accounts only with explicitly granted access or valid admin delegation.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Enable Drive, select narrow file scopes and configure OAuth consent or explicitly shared service-account resources.
3. Implement OAuth redirects/state/PKCE as appropriate, least-privilege scopes, secure token storage, revocation and consent error handling.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement OAuth redirects/state/PKCE as appropriate, least-privilege scopes, secure token storage, revocation and consent error handling.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Prefer file-scoped access when suitable. Drive API permission does not imply access to Gmail or Calendar.

[Reference 1](https://developers.google.com/workspace/drive/api/guides/limits)

## API098 · Google Calendar API

**Developer and workspace integrations · Integration guide**

Read availability and manage events on calendars the identity can access.

[Official setup](https://console.cloud.google.com/apis/library/calendar-json.googleapis.com)

**Credential:** OAuth client ID/configuration and short-lived access tokens; refresh tokens kept securely. Service accounts only with explicitly granted access or valid admin delegation.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Enable Calendar, configure scopes, and obtain user consent or explicit calendar sharing for a service account.
3. Implement OAuth redirects/state/PKCE as appropriate, least-privilege scopes, secure token storage, revocation and consent error handling.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement OAuth redirects/state/PKCE as appropriate, least-privilege scopes, secure token storage, revocation and consent error handling.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Calendar read and write permissions differ. Invitations or event changes are consequential actions and must be authorized.

[Reference 1](https://developers.google.com/workspace/calendar/api/guides/quota)

## API099 · Gmail API

**Developer and workspace integrations · Integration guide**

Read or send email and manage labels with the mailbox owner's permission.

[Official setup](https://console.cloud.google.com/apis/library/gmail.googleapis.com)

**Credential:** OAuth client ID/configuration and short-lived access tokens; refresh tokens kept securely. Service accounts only with explicitly granted access or valid admin delegation.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Enable Gmail, configure the OAuth consent screen and appropriate client, then request only the required mailbox scopes.
3. Implement OAuth redirects/state/PKCE as appropriate, least-privilege scopes, secure token storage, revocation and consent error handling.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement OAuth redirects/state/PKCE as appropriate, least-privilege scopes, secure token storage, revocation and consent error handling.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A standard service account cannot silently read a personal Gmail mailbox. Workspace domain-wide delegation requires administrator approval.

[Reference 1](https://developers.google.com/workspace/gmail/api/quickstart/python) · [Reference 2](https://developers.google.com/workspace/gmail/api/reference/quota)

## API100 · YouTube Data API

**Developer and workspace integrations · Integration guide**

Read video/channel metadata and perform authorized channel-management operations.

[Official setup](https://console.cloud.google.com/apis/library/youtube.googleapis.com)

**Credential:** API key for eligible public data; OAuth 2.0 for user-specific or write operations.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Enable YouTube Data; use a restricted API key for eligible public reads and OAuth consent for private data or channel writes.
3. Keep public reads separate from private writes, use minimal scopes and account for method-specific quota costs.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Keep public reads separate from private writes, use minimal scopes and account for method-specific quota costs.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** API access does not grant video redistribution rights. Upload or channel changes need the channel owner's authorization.

[Reference 1](https://developers.google.com/youtube/v3/getting-started) · [Reference 2](https://developers.google.com/youtube/v3/guides/quota_and_compliance_audits)

## API101 · Google Books API

**Developer and workspace integrations · Integration guide**

Find book metadata, covers and supported previews.

[Official setup](https://console.cloud.google.com/apis/library/books.googleapis.com)

**Credential:** API key for eligible public data; OAuth 2.0 for user-specific or write operations.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a project/key for quota-controlled public lookup; add OAuth only for user-specific library operations.
3. Keep public reads separate from private writes, use minimal scopes and account for method-specific quota costs.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Keep public reads separate from private writes, use minimal scopes and account for method-specific quota costs.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Book metadata is not a license to redistribute the full book. A user's library requires separate consent.

[Reference 1](https://developers.google.com/books/docs/v1/using)

## API102 · JSONPlaceholder

**Testing and educational APIs · Integration guide**

Prototype lists, users and HTTP CRUD interactions without building a backend.

[Official setup](https://jsonplaceholder.typicode.com/)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Call a sample read endpoint and treat POST/PUT/DELETE responses as demonstrations.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Never use it as the database for real customer records or assume test writes persist.

[Reference 1](https://jsonplaceholder.typicode.com/)

## API103 · DummyJSON

**Testing and educational APIs · Integration guide**

Build product, cart and user interfaces with realistic sample structures.

[Official setup](https://dummyjson.com/docs)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Choose the dataset and pagination parameters, and keep sample authentication separate from production identity.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Products, users and credentials are demonstration data, not a production store or authentication service.

[Reference 1](https://dummyjson.com/docs) · [Reference 2](https://dummyjson.com/)

## API104 · Random User Generator

**Testing and educational APIs · Integration guide**

Populate UI prototypes with synthetic-looking user records.

[Official setup](https://randomuser.me/documentation)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Request a bounded number of test records and label them as sample data in demonstrations.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not present generated identities as verified real customers or accounts.

[Reference 1](https://randomuser.me/documentation)

## API105 · httpbin

**Testing and educational APIs · Integration guide**

Inspect HTTP requests, headers, redirects and status-code handling.

[Official setup](https://httpbin.org/)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Use a small request to the method/status endpoint you are testing.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Never send production secrets to a public echo service. Its purpose is protocol testing, not credential validation.

[Reference 1](https://httpbin.org/)

## API106 · PokeAPI

**Testing and educational APIs · Integration guide**

Explore a structured dataset while learning REST or building fan-oriented prototypes.

[Official setup](https://pokeapi.co/docs/v2)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Read the resource schema and cache frequently requested reference records.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Dataset availability does not grant ownership of Pokemon trademarks, artwork or game rights.

[Reference 1](https://pokeapi.co/docs/v2)

## API107 · Open Trivia DB

**Testing and educational APIs · Integration guide**

Retrieve categorized quiz questions for an educational prototype.

[Official setup](https://opentdb.com/api_config.php)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Select a category/difficulty and decode content according to the documented response format.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Review the content license and prevent repeated fetching when a cached question set is sufficient.

[Reference 1](https://opentdb.com/api_config.php)

## API108 · Free Dictionary API

**Testing and educational APIs · Integration guide**

Display supported English definitions, pronunciations and example usage.

[Official setup](https://dictionaryapi.dev/)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Query a supported language/word and handle missing entries gracefully.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Not every word, language or pronunciation will be present. Check the returned audio/content license.

[Reference 1](https://dictionaryapi.dev/)

## API109 · Datamuse

**Testing and educational APIs · Integration guide**

Find related words, rhymes and suggestions for writing or word games.

[Official setup](https://www.datamuse.com/api/)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Choose the word relationship parameters and implement caching/rate limits.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not turn a dated access policy into a permanent promise. It is a lexical helper, not a general LLM.

[Reference 1](https://www.datamuse.com/api/)

## API110 · Crossref REST API

**Research and public datasets · Integration guide**

Resolve DOI metadata and build reference or citation workflows.

[Official setup](https://www.crossref.org/documentation/retrieve-metadata/rest-api/)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Query works/DOIs, provide an application identity/contact and use cursor pagination for large results.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Metadata availability does not imply full-text article access or permission to redistribute paywalled papers.

[Reference 1](https://www.crossref.org/documentation/retrieve-metadata/rest-api/)

## API111 · OpenAlex API

**Research and public datasets · Integration guide**

Analyze scholarly works, authors, institutions and citation relationships.

[Official setup](https://openalex.org/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Register for a key, choose the needed fields and paginate/filter to reduce unnecessary cost.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Large exports and expensive endpoints may consume the allowance quickly. Verify source coverage and record matching.

[Reference 1](https://openalex.org/pricing) · [Reference 2](https://help.openalex.org/api/authentication/) · [Reference 3](https://help.openalex.org/access/pricing/)

## API112 · NASA Open APIs

**Research and public datasets · Integration guide**

Build educational astronomy, image or space-data features.

[Official setup](https://api.nasa.gov/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Request a NASA API key and select the individual service and its data schema.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Different NASA services have different update cycles, data caveats and occasional availability constraints.

[Reference 1](https://api.nasa.gov/) · [Reference 2](https://api.nasa.gov/assets/html/authentication.html)

## API113 · World Bank Indicators API

**Research and public datasets · Integration guide**

Retrieve country-level economic, demographic and development indicators.

[Official setup](https://datahelpdesk.worldbank.org/knowledgebase/articles/889392-about-the-indicators-api-documentation)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Choose indicator/country/date parameters and preserve the metadata and units.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Historical annual indicators are not current live measurements. Compare series only after checking definitions and revisions.

[Reference 1](https://datahelpdesk.worldbank.org/knowledgebase/articles/889392-about-the-indicators-api-documentation)

## API114 · Open Library APIs

**Research and public datasets · Integration guide**

Retrieve book, edition, author and cover metadata.

[Official setup](https://openlibrary.org/developers/api)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Choose search/edition endpoints, identify the application and cache book metadata.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Metadata is not full-book access. Follow rate policy and use bulk exports rather than overwhelming the API.

[Reference 1](https://openlibrary.org/developers/api)

## API115 · USGS Earthquake API

**Research and public datasets · Integration guide**

Query earthquake events by place, time, magnitude and depth.

[Official setup](https://earthquake.usgs.gov/fdsnws/event/1/)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Set a bounded time window, location filters and response format.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A catalog is not earthquake prediction or a guaranteed emergency-alert service. Event data can be revised.

[Reference 1](https://earthquake.usgs.gov/fdsnws/event/1/)

## API116 · USDA FoodData Central

**Research and public datasets · Integration guide**

Search food records and nutrient data for an application.

[Official setup](https://fdc.nal.usda.gov/api-guide/)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Request the data.gov key, choose food types and preserve nutrient units and serving context.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Different foods and data types are not interchangeable. Nutrition records do not provide individualized medical advice.

[Reference 1](https://fdc.nal.usda.gov/api-guide/)

## API117 · NHTSA vPIC

**Research and public datasets · Integration guide**

Decode VINs and retrieve manufacturer or vehicle reference information.

[Official setup](https://vpic.nhtsa.dot.gov/api/)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Choose a VIN/manufacturer operation and validate the country/model-year context.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** This is not a complete parts catalog, vehicle accident history, proof of ownership or guaranteed global model coverage.

[Reference 1](https://vpic.nhtsa.dot.gov/api/)

## API118 · TMDB API

**Media, news and specialist data · Integration guide**

Build film/TV metadata, poster and cast discovery interfaces.

[Official setup](https://developer.themoviedb.org/docs/faq)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Register the application, obtain its key/token and implement required attribution.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** The API does not grant film-streaming rights. Check poster and metadata licensing for the intended commercial product.

[Reference 1](https://developer.themoviedb.org/docs/faq)

## API119 · TVmaze API

**Media, news and specialist data · Integration guide**

Retrieve television series, episode and schedule metadata.

[Official setup](https://www.tvmaze.com/api)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Query series/episode data and preserve attribution and relevant share-alike conditions.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Schedules can change. Metadata access is not access to copyrighted episode video.

[Reference 1](https://www.tvmaze.com/api)

## API120 · football-data.org

**Media, news and specialist data · Integration guide**

Display covered fixtures, standings and teams.

[Official setup](https://www.football-data.org/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a token and check that the required competition and fields belong to the free plan.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Do not advertise universal league coverage or live timing without checking the account's data entitlement.

[Reference 1](https://www.football-data.org/pricing) · [Reference 2](https://www.football-data.org/)

## API121 · Open Food Facts

**Media, news and specialist data · Integration guide**

Look up community food product data by barcode.

[Official setup](https://openfoodfacts.github.io/openfoodfacts-server/api/)

**Credential:** No read secret where permitted; write credentials are separate.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Use identified public reads and caching; create an authorized account only for deliberate product edits.
3. Separate read/write endpoints, identify the application, honor limits and preserve attribution/license obligations.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Separate read/write endpoints, identify the application, honor limits and preserve attribution/license obligations.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Community data can be missing or inaccurate. Preserve license/attribution and do not use it as a safety guarantee.

[Reference 1](https://openfoodfacts.github.io/openfoodfacts-server/api/)

## API122 · Currents News API

**Media, news and specialist data · Integration guide**

Retrieve headlines and news-search metadata for a prototype.

[Official setup](https://currentsapi.services/en)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a key and choose permitted language/search filters.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** API access does not automatically license republishing full articles, photographs or publisher content.

[Reference 1](https://currentsapi.services/en)

## API123 · NewsAPI Developer

**Media, news and specialist data · Integration guide**

Prototype news-headline search during development.

[Official setup](https://newsapi.org/pricing)

**Credential:** Provider-issued API key/token, resource credential or SDK credential; confirm the exact product.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Create a Developer key and keep it limited to an allowed development environment.
3. Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Configure the exact endpoint/SDK, protect server credentials, enforce the chosen scope/plan, then test one small operation.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** An internal production dashboard is still production. Obtain the appropriate plan before deployment.

[Reference 1](https://newsapi.org/pricing) · [Reference 2](https://newsapi.org/terms)

## API124 · AlAdhan API

**Islamic reference services · Integration guide**

Calculate prayer times for a chosen location and date.

[Official setup](https://aladhan.com/prayer-times-api)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Set coordinates/city, date, timezone and calculation method explicitly.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Different calculation methods and local calendars can disagree. Validate the intended local convention before publishing times.

[Reference 1](https://aladhan.com/prayer-times-api)

## API125 · AlQuran Cloud API

**Islamic reference services · Integration guide**

Retrieve Quran verses, surahs and supported editions/translations.

[Official setup](https://alquran.cloud/api)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Choose and pin the edition/translation identifier and validate verse references.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** Review translation provenance and audio/content rights. Do not treat every edition as equivalent.

[Reference 1](https://alquran.cloud/api)

## API126 · MP3Quran API

**Islamic reference services · Integration guide**

Find reciters, recitations and documented audio URLs.

[Official setup](https://www.mp3quran.net/ar/api)

**Credential:** No API secret for this public access path; some services require a descriptive User-Agent or attribution.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Select a documented reciter/riwayah and use the API's current stream/file references.
3. Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Implement the public request, validation, timeouts, caching, attribution and policy-specific rate limits.

**Monitoring:** Record the product-specific unit and account scope. A public usage/balance API has not been established for this entry; consult its dashboard or documented reporting endpoint.

**Caveat:** A publicly accessible recording URL is not automatically permission to resell or rehost the recording.

[Reference 1](https://www.mp3quran.net/ar/api)

## API127 · Ollama Local API

**Self-hosted software · Integration guide**

Run compatible language models locally and expose a local API.

[Official setup](https://docs.ollama.com/api/introduction)

**Credential:** Local administrator/API credentials that you configure; model/download tokens only when required by the source.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Install Ollama, download a hardware-appropriate local model, disable cloud routing when required, and protect the local server.
3. Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.

**Monitoring:** Measure requests, latency, CPU/GPU, RAM, disk and optional model tokens. Local software has no provider-funded balance unless you connect another service.

**Caveat:** Local installation is manual. A cloud model selected through a local client is not local-only inference.

[Reference 1](https://docs.ollama.com/api/introduction)

## API128 · LibreTranslate Self-hosted

**Self-hosted software · Integration guide**

Operate your own text-translation service using supported installed language models.

[Official setup](https://docs.libretranslate.com/)

**Credential:** Local administrator/API credentials that you configure; model/download tokens only when required by the source.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Install the project, select language models, configure API-key enforcement and place it behind authenticated HTTPS.
3. Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.

**Monitoring:** Measure requests, latency, CPU/GPU, RAM, disk and optional model tokens. Local software has no provider-funded balance unless you connect another service.

**Caveat:** Translation quality and language coverage depend on installed models. Review the software/model license before commercial deployment.

[Reference 1](https://docs.libretranslate.com/)

## API129 · PocketBase

**Self-hosted software · Integration guide**

Build a lightweight backend with accounts, records, files and realtime updates.

[Official setup](https://pocketbase.io/docs/)

**Credential:** Local administrator/API credentials that you configure; model/download tokens only when required by the source.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Install the server, define collections/rules, create admin credentials and configure HTTPS/backups.
3. Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.

**Monitoring:** Measure requests, latency, CPU/GPU, RAM, disk and optional model tokens. Local software has no provider-funded balance unless you connect another service.

**Caveat:** Review current version/migration guidance before critical production use. A local demo is not hardened deployment.

[Reference 1](https://pocketbase.io/docs/)

## API130 · LocalAI

**Self-hosted software · Integration guide**

Expose compatible AI inference APIs backed by models you operate.

[Official setup](https://localai.io/)

**Credential:** Local administrator/API credentials that you configure; model/download tokens only when required by the source.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Install LocalAI, configure a supported backend/model, set API authentication and test locally before exposing it.
3. Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.

**Monitoring:** Measure requests, latency, CPU/GPU, RAM, disk and optional model tokens. Local software has no provider-funded balance unless you connect another service.

**Caveat:** The API surface does not guarantee every model supports tools, vision, speech or all response formats.

[Reference 1](https://localai.io/)

## API131 · whisper.cpp Server

**Self-hosted software · Integration guide**

Transcribe speech using a local Whisper model and HTTP server.

[Official setup](https://raw.githubusercontent.com/ggml-org/whisper.cpp/master/examples/server/README.md)

**Credential:** Local administrator/API credentials that you configure; model/download tokens only when required by the source.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Build/install whisper.cpp, download the chosen model, configure server authentication through a proxy and validate accepted audio formats.
3. Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.

**Monitoring:** Measure requests, latency, CPU/GPU, RAM, disk and optional model tokens. Local software has no provider-funded balance unless you connect another service.

**Caveat:** Latency and language accuracy must be measured on the actual hardware. Do not promise real-time throughput from software availability alone.

[Reference 1](https://raw.githubusercontent.com/ggml-org/whisper.cpp/master/examples/server/README.md)

## API132 · Kokoro-FastAPI

**Self-hosted software · Integration guide**

Expose supported local text-to-speech generation through an API.

[Official setup](https://github.com/remsky/Kokoro-FastAPI)

**Credential:** Local administrator/API credentials that you configure; model/download tokens only when required by the source.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Install the compatible runtime/model, review available voices/languages and protect the server endpoint.
3. Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.

**Monitoring:** Measure requests, latency, CPU/GPU, RAM, disk and optional model tokens. Local software has no provider-funded balance unless you connect another service.

**Caveat:** Do not assume Arabic or a particular voice is supported. Verify both model and voice rights.

[Reference 1](https://github.com/remsky/Kokoro-FastAPI)

## API133 · ComfyUI Local Server

**Self-hosted software · Integration guide**

Execute local image/video workflows and connect them to an application.

[Official setup](https://github.com/Comfy-Org/ComfyUI)

**Credential:** Local administrator/API credentials that you configure; model/download tokens only when required by the source.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Install ComfyUI and audited model/node dependencies, build a workflow, then expose only a protected backend integration.
3. Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.

**Monitoring:** Measure requests, latency, CPU/GPU, RAM, disk and optional model tokens. Local software has no provider-funded balance unless you connect another service.

**Caveat:** Custom nodes execute code and need review. A workflow may call paid external services despite a free local interface.

[Reference 1](https://github.com/Comfy-Org/ComfyUI)

## API134 · Qdrant Self-hosted

**Self-hosted software · Integration guide**

Operate your own vector store for search and RAG.

[Official setup](https://qdrant.tech/documentation/quickstart/)

**Credential:** Local administrator/API credentials that you configure; model/download tokens only when required by the source.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Deploy Qdrant, create protected storage/collections and configure keys, TLS and backups.
3. Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.

**Monitoring:** Measure requests, latency, CPU/GPU, RAM, disk and optional model tokens. Local software has no provider-funded balance unless you connect another service.

**Caveat:** Local cluster sizing and high availability are your responsibility; do not expose an unauthenticated database publicly.

[Reference 1](https://qdrant.tech/documentation/quickstart/)

## API135 · Chroma Self-hosted

**Self-hosted software · Integration guide**

Store embeddings and retrieve relevant document chunks in a controlled environment.

[Official setup](https://docs.trychroma.com/docs/overview/introduction)

**Credential:** Local administrator/API credentials that you configure; model/download tokens only when required by the source.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Install the required deployment mode, persist data and enforce server access control before network exposure.
3. Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.

**Monitoring:** Measure requests, latency, CPU/GPU, RAM, disk and optional model tokens. Local software has no provider-funded balance unless you connect another service.

**Caveat:** A prototype persistence directory is not a complete production backup or access-control strategy.

[Reference 1](https://docs.trychroma.com/docs/overview/introduction)

## API136 · Meilisearch Self-hosted

**Self-hosted software · Integration guide**

Provide typo-tolerant search and filters over application data.

[Official setup](https://www.meilisearch.com/docs/resources/self_hosting/getting_started/quick_start)

**Credential:** Local administrator/API credentials that you configure; model/download tokens only when required by the source.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Install the server, protect the master key, define index settings and expose only scoped search credentials.
3. Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.

**Monitoring:** Measure requests, latency, CPU/GPU, RAM, disk and optional model tokens. Local software has no provider-funded balance unless you connect another service.

**Caveat:** Indexing and search keys have different privileges. Check memory/storage demands and backup procedures.

[Reference 1](https://www.meilisearch.com/docs/resources/self_hosting/getting_started/quick_start)

## API137 · Typesense Self-hosted

**Self-hosted software · Integration guide**

Build fast faceted search over product or document collections.

[Official setup](https://typesense.org/docs/)

**Credential:** Local administrator/API credentials that you configure; model/download tokens only when required by the source.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Deploy Typesense, configure schemas and restricted search-only keys, and set up snapshots/backups.
3. Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.

**Monitoring:** Measure requests, latency, CPU/GPU, RAM, disk and optional model tokens. Local software has no provider-funded balance unless you connect another service.

**Caveat:** Do not expose administrative API keys through the client. Cluster reliability requires deliberate deployment design.

[Reference 1](https://typesense.org/docs/)

## API138 · Keycloak

**Self-hosted software · Integration guide**

Operate identity, SSO and OAuth/OIDC services under your control.

[Official setup](https://www.keycloak.org/)

**Credential:** Local administrator/API credentials that you configure; model/download tokens only when required by the source.

1. Confirm the official product, allowed purpose, current plan and relevant region.
2. Deploy a production database and Keycloak, create a realm/client, configure HTTPS/redirects and set administrative access.
3. Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.
4. Run one minimal, non-sensitive test after authorization; inspect status, usage units and any charge before broader use.

**Implementation:** Install a versioned release, bind privately, configure authentication/TLS, provision storage/models and verify a local health check.

**Monitoring:** Measure requests, latency, CPU/GPU, RAM, disk and optional model tokens. Local software has no provider-funded balance unless you connect another service.

**Caveat:** Federating Google login is optional and separately configured. Running an identity server creates security and recovery obligations.

[Reference 1](https://www.keycloak.org/)
