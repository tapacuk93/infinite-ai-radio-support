# Privacy Policy

**Last updated: 2026-07-20**

Infinite AI Radio (iPhone, iPad, and Mac) is designed to collect as little data as possible. This policy explains exactly what the app does and does not do with your information, and applies the same way on every platform.

## Data we don't collect

Infinite AI Radio has no backend server of its own, no user accounts, and no analytics or tracking SDKs. We (the developer) do not receive, store, or have access to your topics, listening history, API keys, or location.

## Your API keys

The app can use your own API keys for Anthropic (required), and optionally ElevenLabs, OpenAI (DALL-E), and Stability AI if you turn on those features in Settings. Each key is:
- Stored only on your device (or synced via your own iCloud account if iCloud sync is on — see below — never to any server we control).
- Sent only directly to that provider's own API (`api.anthropic.com`, `api.elevenlabs.io`, `api.openai.com`, or `api.stability.ai`), never to us or any other server.

Usage of each key is billed directly by that provider to your own account.
- [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy)
- [ElevenLabs' privacy policy](https://elevenlabs.io/privacy)
- [OpenAI's privacy policy](https://openai.com/privacy)
- [Stability AI's privacy policy](https://stability.ai/privacy-policy)

## Topics and broadcast content

Whatever topic you type in, and the resulting generated text, is sent to Anthropic's API to produce the broadcast, and is processed under Anthropic's own data-handling policy (see link above). If you've turned on ElevenLabs narration and/or DALL-E or Stability AI images in Settings, the segment text or image prompt is also sent to that provider's API to generate the voice audio or artwork. This content is never sent anywhere else.

Your station history (the topics you've tuned to, how deep you dove into each, and any facts you've saved) is stored locally on your device, so it's available across app launches. If iCloud sync is turned on (Settings, on by default), this history and your app preferences are also synced through your own iCloud account so they carry over to your other devices — your API keys are deliberately excluded from that sync. This data is only ever accessible to you, through your own iCloud account; we have no access to it.

## Images

To show a relevant photo alongside a broadcast, the app either:
- Asks Claude to run a web search on your behalf (through the same `api.anthropic.com` connection as above),
- Fetches a quick preview thumbnail from Wikipedia, if you've enabled the "fast image previews" toggle in Settings, or
- Generates an image via OpenAI's DALL-E or Stability AI's API, if you've enabled and configured one of those in Settings.

Either way, only the topic/subject text needed to find or generate a matching photo is sent — never your API key.

## Location

If you allow it, the app makes a one-shot, reduced-accuracy location request purely to personalize the "Suggested for you" station list with a city/region-level hint (e.g. local news or weather). This lookup is resolved to a city and country name via Apple's own geocoding service and is never sent to us or to any AI provider tied to your identity. Denying location access simply means suggestions skip that personalization.

## Apple Music

If you turn on the optional background music bed in Settings, the app uses Apple's MusicKit to play a track from your Apple Music subscription underneath the narration. This is handled entirely by Apple's own MusicKit framework under your Apple ID — we never see what plays.

## Subscriptions

Infinite AI Radio offers an optional auto-renewing subscription, sold and processed entirely by Apple through StoreKit. We never see or store your payment details — Apple handles billing, receipts, and renewal directly. See Apple's own [Privacy Policy](https://www.apple.com/legal/privacy/) and the Terms of Use linked in the app for how Apple handles subscription and payment data.

## Third parties

The only third parties involved are:
- **Anthropic** (`api.anthropic.com`) — generates the broadcast text and, when relevant, runs image searches.
- **ElevenLabs** (`api.elevenlabs.io`) — only if you enable external voice narration, to generate spoken audio from segment text.
- **OpenAI** (`api.openai.com`) — only if you enable and configure DALL-E images, to generate artwork from an image prompt.
- **Stability AI** (`api.stability.ai`) — only if you enable and configure Stability AI images, to generate artwork from an image prompt.
- **Wikipedia** (`wikipedia.org`) — only when the optional fast-preview toggle is on, to fetch a preview thumbnail.
- **Apple** — iCloud (if sync is on), MusicKit (if the music bed is on), and StoreKit (for the subscription), all under your own Apple ID and governed by Apple's own privacy policy.

We don't share data with anyone else, and we don't sell data — there's no data collected on our end to sell.

## Changes to this policy

If this policy changes, the update will be posted here with a new "Last updated" date.

## Contact

Questions about this policy? Email **tapacuk93@gmail.com** or [open an issue](https://github.com/tapacuk93/infinite-ai-radio-support/issues).
