---
layout: default
title: 随口成章 Help
permalink: /help-en/
---

# Your first successful dictation

[Download 随口成章](https://apps.apple.com/us/app/xx-voice-input/id6773677051) · [中文帮助](../help/) · [1.0.6 privacy policy](../privacy-1.0.6-en/)

This guide covers version 1.0.6, currently available through TestFlight. Check the App Store for the current public release. App pricing is shown in your App Store; third-party API usage is billed separately.

## Start with direct transcription

1. Open the app and follow onboarding. Allow microphone access and, for Apple recognition, speech recognition access.
2. In iPhone Settings, open General → Keyboard → Keyboards → Add New Keyboard. Add 随口成章 and allow Full Access so the keyboard and host app can share recording state and results.
3. Return to onboarding. Use the globe button to switch to the xx keyboard in the practice field.
4. Choose direct transcription and dictate a short sentence. If microphone activation opens the host app, follow its instructions to return to your previous app.
5. Stop recording and check that your words appear. Some apps, password fields, and restricted text fields do not allow third-party keyboards.

Apple recognition does not require your own AI API key. Availability depends on the device, language, and system service. Strict offline mode refuses cloud fallback and shows an error when on-device recognition is unavailable.

## Add AI text processing

Speech recognition handles your audio. AI text processing handles the transcription. They are configured separately.

1. Create a key in your chosen provider's API console. Confirm your API credits, base URL, and model ID. A chat subscription may not include API credits.
2. Open Provider Settings → AI text processing. Select the service and enter the required details.
3. Review the cloud processing prompt. Polishing, translation, and prompt organization send your transcription to the configured provider. BYOK does not provide anonymity or guarantee zero retention.
4. Tap Send test sample. This sends a fixed example, without recording or reading history, and may incur a small API usage fee.
5. After the test succeeds, choose a processing mode in the keyboard and try another dictation.

Available providers depend on the released App Store build. Ollama requires your own reachable model server. On iPhone, `localhost` means the phone itself, not your Mac.

## Troubleshooting

- **Keyboard missing:** Check that it was added, use the globe button, and try an ordinary text field.
- **The host app opens:** Activate the microphone and follow the return instructions. A released or interrupted background session may need activation again.
- **Authentication failure:** Check the API key and service permissions. Do not enter your chat account password.
- **Request limited:** Check provider quota, billing, and rate limits before retrying.
- **Model or endpoint error:** Use the provider's API base URL and exact model ID. Do not append `chat/completions` yourself.
- **Original text returned:** AI processing failed, but your transcription was preserved. Review the error and service configuration.
- **Offline recognition unavailable:** Check device/language support or select an available downloaded local engine.

## Privacy and deletion

The home screen explains the current data flow. Local history defaults to 10 minutes; disabling history clears existing records. Delete service keys in Provider Settings, or use Erase All Data in About for app-managed data. Data already received by a provider follows that provider's rules.

## Contact

Email carlliuxx@gmail.com with your app version, iOS version, mode, provider name, and reproduction steps. Do not include API keys, passwords, or sensitive recordings. A fictional short sentence is usually enough.


## Free dictation and optional PRO

Version 1.0.6 offers free basic dictation and 30 successful AI refinements per installation. Failed or cancelled requests do not count. Continue AI refinement with a one-time PRO purchase (US base price $1.99; local prices are shown by the App Store). Bring your own API key; third-party provider usage is separate. The home-screen allowance row opens the purchase and Restore Purchases controls. Version 1.0.6 was submitted for App Store review on October 7, 2026 and is awaiting review; availability follows the store listing.
