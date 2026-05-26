---
layout: default
title: xx Voice Keyboard — Privacy Policy
permalink: /en/
---

# xx Voice Keyboard — Privacy Policy

**Last updated**: May 26, 2026
**Effective date**: First App Store release

xx Voice Keyboard ("the App") is operated independently by an individual developer. We take your privacy seriously. This policy explains what information the App processes and how. **Please read carefully before using the App.**

## 1. Who we are

- **Developer**: Independent developer (Individual Developer account)
- **Contact**: carlliuxx@gmail.com
- **Scope**: A third-party voice-input keyboard for iOS
- **Initial availability**: Worldwide except mainland China

> The developer's legal name is shown on the App Store product page under the "Developer" field.

## 2. Information we process

All processing is strictly limited to the App's core function — converting your speech into text — and follows the principle of data minimization.

### 2.1 Microphone audio

| Item | Detail |
|---|---|
| Data type | Microphone audio stream (PCM 16 kHz) |
| Trigger | Only when you actively tap the keyboard mic button or use the in-app test recording |
| Handling | Used immediately for recognition; **discarded right after, with no persistent local or cloud copy** |
| Leaves the device? | Depends on the engine you select (see §2.4) |
| Linked to identity? | No. We do not bind audio to any identifying field (name, email, device ID, etc.) |

### 2.2 Recognized text

| Item | Detail |
|---|---|
| Data type | Text returned by the speech-recognition engine |
| Handling | Saved in the main App's local history (default 7-day retention, adjustable / clearable in settings) |
| Leaves the device? | No. Recognized text stays in the device's App Group sandbox |

### 2.3 App configuration

| Item | Detail |
|---|---|
| Content | Selected engine, hot words, vocabulary, language preference, etc. |
| Storage | Local — `~/Library/Group Containers/group.com.xx.xxvoice.shared/` and iOS Keychain |
| Leaves the device? | No |

### 2.4 Third-party recognition services

The App offers two recognition paths. **You choose** in the main App's settings:

#### Apple Speech Recognition (default)
- Provided by Apple
- Audio may be sent to Apple servers for recognition (some languages run on-device)
- Governed by Apple's own privacy policy: <https://www.apple.com/legal/privacy/>
- We do not read, store, or analyze anything on this path

#### Volcano Engine speech recognition (optional, behind an in-app "Cloud ASR" toggle)
- Provider: Beijing Volcano Engine Technology Co., Ltd. (a ByteDance company)
- Governed by: <https://www.volcengine.com/docs/6561/107708>
- Only when **you explicitly enable** the Cloud ASR toggle and pick Volcano does the App send microphone audio over HTTPS/WebSocket to Volcano servers for recognition
- We send only the audio stream — no name, device ID, IDFA, IDFV, or any identity field beyond the IP address required by HTTPS
- Volcano returns text to the App
- You can disable Cloud ASR at any time; all recognition then falls back to Apple Speech

**Important**: The first time you enable Cloud ASR, the App shows an explicit consent dialog. **No audio leaves the device without your consent.**

## 3. What we never do

We commit that we will not:

- Collect your name, email, phone, address, birthday, or gender
- Access your location, contacts, photos, calendar, or health data
- Log every keystroke you type (only voice-recognized text is saved as history)
- Bundle any advertising, analytics, or tracking SDK
- Use your data to train AI models
- Sell, rent, or trade your data to any third party
- Track you across apps (NSPrivacyTracking = false)

## 4. The keyboard extension's "Full Access"

To deliver voice input, the keyboard extension requires you to enable **Allow Full Access** in iOS Settings → General → Keyboard → xx Voice Keyboard. "Full Access" is used solely for:

- Sharing audio-recognition state and result text between the keyboard extension and the main App via App Group
- **Nothing else**
- The keyboard extension itself **does not make any network calls** — only the main App does, and only when you have enabled Cloud ASR

## 5. Retention & deletion

- **Audio**: discarded immediately after recognition; no persistent copy anywhere
- **Recognition history**: auto-purged after 7 days by default; clear manually anytime in main App → History
- **Configuration**: removed by iOS when you uninstall the App; Keychain items are cleared too

## 6. Children's privacy

The App is not directed at children under 13 and we do not knowingly collect their data.

## 7. Your rights

You can:

- Access your local data (view history and configuration in the main App)
- Delete it (clear history, turn off features, uninstall)
- Withdraw consent (toggle off Cloud ASR or revoke keyboard Full Access)
- Reach us with privacy questions via the email above

## 8. Updates to this policy

If this policy changes, we will notify you via in-app notice or the App Store update notes. Material changes will be communicated with a reasonable advance period before they take effect.

## 9. Contact

For any privacy-related question, email **carlliuxx@gmail.com**.
