---
layout: default
title: 随口成章 Privacy Policy
permalink: /privacy-1.0.6-en/
---

# 随口成章 Privacy Policy

Revised: October 8, 2026. Applies to version 1.0.6 when released.

## Where processing happens

随口成章 is operated by an independent developer. It provides speech transcription and optional AI text processing without requiring a developer account. Speech recognition and AI text processing are separate steps.

- Paraformer and SenseVoice process speech on your device after the relevant model is downloaded.
- Apple Speech prefers on-device recognition when your device and language support it. Standard mode may also use Apple services. Strict offline mode does not fall back to cloud recognition; unsupported configurations show an error.
- Cloud speech recognition sends audio to your selected speech provider.
- Polishing, translation, and prompt organization send the transcription to your configured AI service. Direct transcription and offline mode skip AI text processing.
- Ollama connects to a model server you configure. It is not an AI model bundled on your iPhone; text is sent to the configured server address.

The app connects to these services directly rather than using a developer-operated audio/text relay. Model downloads, help links, and external websites also connect to their respective hosts.

## Credentials and third-party services

You supply your API credentials. The app saves keys in the iOS Keychain. Newly saved keys are excluded from ordinary preferences and do not enable Keychain cloud synchronization. During upgrades, legacy keys are migrated and their preferences copies removed after secure storage succeeds. If Keychain is unavailable, the legacy copy is retained and migration is retried on a later launch to avoid losing your configuration.

Keys authenticate requests to your selected services. BYOK does not provide anonymity: a provider may associate API accounts, network addresses, and the audio or text you send. Retention, training, billing, and other provider practices depend on their policies and your account settings. The developer cannot promise zero retention or no training on their behalf.

Volcano speech requests use a random request identifier instead of reading IDFV for that field. The app does not replace it with an advertising identifier or device fingerprint.

## Local records and system surfaces

History is retained for 10 minutes by default. You can change the duration, disable history, or clear it. Expired records are pruned during reads, writes, active use, and resumed use. iOS may suspend the app, so cleanup is not guaranteed at the exact expiry second. Disabling history also clears existing history.

During dictation, the app holds current results in memory and shared App Group state for keyboard insertion. The keyboard clears the matching shared result after consuming it. Disabling history does not eliminate all temporary processing copies. Live Activities and the lock screen may display recording status and partial text. If you enable the clipboard fallback, text may be copied to the system clipboard when insertion fails.

Debug logging is off by default. When enabled, logs help diagnose state, timing, and errors; you can set retention or clear them. Review diagnostic information before sharing it with support. History and logs are not automatically sent to the developer.

## Permissions

Microphone permission is used for dictation you initiate. Apple recognition also requests speech recognition permission. Keyboard Full Access enables sharing state and results with the host app. It does not cause this keyboard to read everything you type with other keyboards. System restrictions and app or field settings can limit third-party keyboard availability.

## Choices and deletion

You can switch services, revoke cloud authorization, choose strict offline mode, delete current service keys, or clear history. Erase All Data in About clears app-managed history, settings, logs, downloaded models, and Keychain entries. Uninstalling is not a guarantee that Keychain entries are deleted; use the in-app deletion controls before uninstalling.

In-app deletion does not delete data already received by third parties, text you copied elsewhere, or existing system backups. Contact the relevant provider for its deletion process.

## Contact

Privacy and support: carlliuxx@gmail.com. The product is distributed in available App Store territories outside mainland China.


## Purchases and free allowance

The app uses Apple StoreKit for a one-time purchase, restoring purchases, and verifying access. Apple processes payment; the developer does not receive card details or payment passwords. The app reads Apple-verified purchase status to determine access to AI Refinement PRO. Apple manages purchase and refund records under its policies.

The free AI-refinement counter is stored on this device. No developer account, advertising identifier, or device fingerprint is used to count usage across devices. The keyboard and host share an availability hint and remaining allowance; the host checks the actual entitlement. Erasing app data or uninstalling may reset the allowance but does not revoke a valid Apple-managed purchase. Restore Purchases can retrieve that entitlement again.

The one-time app unlock includes no third-party AI or speech credits. Users provide their own API keys and pay their chosen providers' usage fees.

## Explicit permission for third-party AI sharing (build 12 onward)

Before enabling a new speech service or AI server address, a dedicated permission screen identifies the recipient, full server address, data and purpose, and requires an affirmative “Allow sharing with this recipient” action. Permission is off by default. Entering an API key, granting microphone access or enabling keyboard Full Access does not grant third-party AI permission. Legacy global permissions are not carried forward.

- Cloud speech sends audio you record, configured vocabulary, language and recognition settings to Volcano/ByteDance at openspeech.bytedance.com for transcription. Service credentials authenticate the request.
- AI text processing sends the current transcript, text you type or paste and explicitly submit, or the original of one history item you explicitly reprocess, plus the selected instructions, target language and model settings to your chosen AI service for polishing, translation, prompts, key points, tasks or voice edits. A voice edit also sends the previous text you ask to revise and the spoken edit instruction as text. It does not send raw audio to text models or automatically upload your whole history. Connection tests send only a fixed sample.
- Providers receive API credentials for authentication and can see network addresses. The app adds no advertising identifier and does not relay or upload audio, text or API keys to the developer.

Available AI recipients are Doubao/ByteDance ARK, MiniMax, Alibaba Cloud Bailian, Kimi/Moonshot, OpenRouter, OpenAI, Gemini/Google, DeepSeek, Zhipu, Claude/Anthropic, or the operator of your configured Ollama/compatible API server. The permission screen shows the actual address. A custom address is not assumed to belong to the brand selected in the menu. OpenRouter may route requests onward to the selected model provider; check its routing and data policies as well.

Permission is specific to data purpose, provider and address and covers both app and keyboard. An unapproved provider or address requires new permission. Text-service redirects are refused. Declining leaves basic Apple dictation available. Revoke in Provider Settings to stop subsequent sharing. Revoking does not erase information already received by a provider; use that provider’s deletion process.

### Third-party protection requirements

We require authorized data processors to provide the same or equivalent personal-data protection described here, including purpose limitation, appropriate transport and storage security, access controls, and applicable retention and deletion mechanisms. The app sends only the data needed for the request to the recipient you explicitly choose and authorize. Review your service’s privacy policy, data-processing terms, retention and training settings before granting access. Do not authorize or use a custom server unable to provide these protections.

User-configured services are controlled by independent operators. We cannot promise zero retention or no training on their behalf, and do not claim every account or custom server has been independently audited. Do not submit personal data you lack permission to share or sensitive material unsuitable for the service’s protection level. Revoke access and contact us if you identify a protection issue.

## First-use disclosure and renewed permission (build 21)

The first-use flow shows Data & Privacy before keyboard setup. Continuing setup does not grant third-party AI permission. You can also open Home → Data Sharing & AI Permission to see the configured recipient and address, review the separate audio/text permission, or revoke it. The updated disclosure requires a new explicit choice even if you authorized an earlier build. Declining AI permission does not prevent entering the app or using Apple direct transcription.
