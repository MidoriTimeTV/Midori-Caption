# Midori Caption Privacy Notice

Effective date: September 8, 2026  
Last updated: September 17, 2026

This notice explains how the Windows application “Midori Caption” (the “Application”), provided by MidoriTimeTV, handles information.

## 1. General Approach

The Application is designed to operate primarily on the user’s device.

MidoriTimeTV does not operate a proprietary server that collects users’ audio, captions, user dictionaries, API keys, or usage data through the Application.

The Application does not include telemetry that automatically sends audio, captions, usage data, or device information to MidoriTimeTV.

Network communication occurs only when a user enables a feature that requires an external service.

## 2. Speech Recognition

Japanese speech recognition and voice activity detection are generally performed on the user’s device.

For normal live-caption use, microphone audio is not sent to MidoriTimeTV or to translation APIs for speech recognition.

The live-caption feature does not automatically save microphone audio as recording files.

## 3. Captions and OBS

Recognition results and captions are generally processed on the user’s device.

When OBS integration is used, captions are provided to the OBS Browser Source through a local caption server, normally using `127.0.0.1`.

The Browser Source URL may contain an access token and should not be exposed in streams, recordings, screenshots, or screen sharing.

## 4. Local Translation

When local translation is selected, the relevant translation is performed on the user’s device and the text is not sent to an external translation API for that translation operation.

Required translation models may be downloaded over HTTPS from their distribution source when the feature is first enabled.

The model provider may receive ordinary network information such as IP address, request time, and requested files.

## 5. External Translation Services

If the user enables an external translation service, finalized Japanese text, target-language information, and other data required for translation are sent to the selected service.

Supported services may include DeepL, Google Cloud Translation, Microsoft Azure Translator, OpenAI, and other services clearly identified by the Application.

Caption text is not sent to translation services the user did not select.

If OpenAI is used, the Application may send up to two immediately preceding finalized utterances together with the current utterance for contextual translation.

Data handled by external services is subject to those providers’ terms, privacy policies, account settings, and contracts.

## 6. API Keys, Passwords, and OAuth Credentials

API keys, OBS WebSocket passwords, OAuth tokens, and other credentials are obtained or authorized by the user.

Credentials stored by the Application are designed to be protected using Windows DPAPI or equivalent operating-system protection so that they can normally be decrypted only by the same Windows user.

MidoriTimeTV does not operate a proprietary server for collecting or storing these credentials.

Settings exports are designed not to include API keys, passwords, OAuth access tokens, refresh tokens, or similar secrets.

## 7. Discord Integration

Discord integration is optional and operates only after the user explicitly enables or authorizes it.

For speaker labeling or other clearly disclosed features, the Application may process limited metadata such as:

- Discord User ID
- display name
- voice-channel membership
- speaking start/stop state
- other minimal voice-state metadata required for speaker labeling

The Application is not intended to access DMs, message content, or message history for speaker labeling.

The Application is not designed to obtain Discord call audio itself from Discord RPC or equivalent speaker-state integration.

Speaking-state information may be matched locally against VAD/ASR timestamps from audio captured on the user’s device in order to label captions with the current speaker.

Discord User IDs, display names, and speaking states are not automatically transmitted to a MidoriTimeTV-controlled server.

Disabling or disconnecting Discord integration stops the Application from collecting new Discord events.

Discord’s own handling of information is governed by Discord’s terms and privacy policy.

## 8. Google Fonts

If Google Fonts features are used, the Application or OBS Browser Source may connect to Google servers.

When local storage is selected, font files are downloaded to the device. When cloud loading is selected, OBS Browser Sources or similar components may connect to Google Fonts while captions are displayed.

## 9. Information Stored on the Device

The Application may store settings, user dictionaries, translation terminology dictionaries, encrypted credentials, diagnostic logs, font caches, WebView2 data, speech-recognition models, VAD models, and local translation models on the device.

Data is mainly stored under `%LOCALAPPDATA%\MidoriCaption`.

Some settings and dictionaries may be stored in plain text.

## 10. Diagnostic Logs

The Application may store diagnostic logs locally for troubleshooting and performance verification.

Logs may include timestamps, operation names, error categories, processing times, selected translation method, OBS scene/source names, and model status.

The Application is designed not to intentionally log API keys, passwords, OAuth tokens, microphone audio, or caption text.

Diagnostic logs are not automatically sent to MidoriTimeTV.

## 11. Sale or Disclosure of Data

Because MidoriTimeTV does not operate a proprietary server that collects users’ audio, captions, or usage data through the Application, MidoriTimeTV does not sell such information to third parties.

When users enable services such as translation APIs, Google Fonts, Discord, or OBS, information may be exchanged between the user and those service providers according to the user’s settings and actions.

## 12. Future Features

If future versions add new data-processing features such as video/audio-file transcription, online accounts, automatic crash reporting, or telemetry, this notice will be updated as appropriate before or when those features are introduced.

## 13. Changes to This Notice

This notice may be updated when the Application or its information-handling practices change.

Material changes may be announced in the Application or on the public documentation page where appropriate.

## 14. Contact

MidoriTimeTV  
Email: midoritimetv@gmail.com
