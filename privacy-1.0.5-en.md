---
layout: default
title: xx Voice Input Privacy Policy
permalink: /privacy-1.0.5-en/
---

# xx Voice Input Privacy Policy

Revised: October 6, 2026. Applies to version 1.0.5 when released.

## Where processing happens

xx Voice Input is operated by an independent developer. It provides speech transcription and optional AI text processing without requiring a developer account. Speech recognition and AI text processing are separate steps.

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
