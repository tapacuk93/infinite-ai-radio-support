# Privacy Policy

**Last updated: 2026-07-23**

Infinite AI Radio (iPhone, iPad, and Mac) is designed to collect as little data as possible. This policy explains exactly what the app does and does not do with your information, and applies the same way on every platform.

## Data we don't collect

Infinite AI Radio has no backend server of its own, no user accounts, and no analytics or tracking SDKs. We (the developer) do not receive, store, or have access to your topics, listening history, or API keys.

## Your API keys

In Settings, you can pick which AI narrates the broadcast — Claude (Anthropic), OpenAI, Gemini (Google), Grok (xAI), or DeepSeek — and enter that provider's own API key. You can optionally add further keys to enable ElevenLabs narration and/or OpenAI (DALL-E) or Stability AI image generation. Each key is:
- Stored only on your device (or synced via your own iCloud account if iCloud sync is on — see below — never to any server we control).
- Sent only directly to that provider's own API (`api.anthropic.com`, `api.openai.com`, `generativelanguage.googleapis.com`, `api.x.ai`, `api.deepseek.com`, `api.elevenlabs.io`, or `api.stability.ai`), never to us or any other server.

Usage of each key is billed directly by that provider to your own account.
- [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy)
- [OpenAI's privacy policy](https://openai.com/privacy)
- [Google's privacy policy](https://policies.google.com/privacy)
- [xAI's privacy policy](https://x.ai/legal/privacy-policy)
- [DeepSeek's privacy policy](https://www.deepseek.com/en/privacy-policy)
- [ElevenLabs' privacy policy](https://elevenlabs.io/privacy)
- [Stability AI's privacy policy](https://stability.ai/privacy-policy)

## Topics and broadcast content

Whatever topic you type in, and the resulting generated text, is sent to whichever AI provider you've selected as your main narrator, and is processed under that provider's own data-handling policy (see links above). If you've turned on ElevenLabs narration and/or DALL-E or Stability AI images in Settings, the segment text or image prompt is also sent to that provider's API to generate the voice audio or artwork. This content is never sent anywhere else.

Your station history (the topics you've tuned to, how deep you dove into each, and any facts you've saved) is stored locally on your device, so it's available across app launches. If iCloud sync is turned on (Settings, on by default), this history and your app preferences are also synced through your own iCloud account so they carry over to your other devices — your API keys are deliberately excluded from that sync. This data is only ever accessible to you, through your own iCloud account; we have no access to it.

## Images

To show a relevant photo alongside a broadcast, the app either:
- Asks Claude to run a web search on your behalf (through `api.anthropic.com`) whenever you have an Anthropic key entered — even if you've picked a different provider to narrate — or
- Fetches a quick preview thumbnail from Wikipedia if no Anthropic key is available (or if you've enabled the "fast image previews" toggle in Settings), or
- Generates an image via OpenAI's DALL-E or Stability AI's API, if you've enabled and configured one of those in Settings.

Either way, only the topic/subject text needed to find or generate a matching photo is sent — never your API key.

## Subscriptions

Infinite AI Radio offers an optional auto-renewing subscription, sold and processed entirely by Apple through StoreKit. We never see or store your payment details — Apple handles billing, receipts, and renewal directly. See Apple's own [Privacy Policy](https://www.apple.com/legal/privacy/) and the Terms of Use linked in the app for how Apple handles subscription and payment data.

## Third parties

The only third parties involved are:
- **Anthropic** (`api.anthropic.com`) — generates the broadcast text if Claude is your chosen main AI, and, whenever an Anthropic key is entered, runs image searches regardless of which AI you've chosen to narrate.
- **OpenAI** (`api.openai.com`) — generates the broadcast text if OpenAI is your chosen main AI, and/or generates artwork if you enable and configure DALL-E images.
- **Google** (`generativelanguage.googleapis.com`) — generates the broadcast text if Gemini is your chosen main AI.
- **xAI** (`api.x.ai`) — generates the broadcast text if Grok is your chosen main AI.
- **DeepSeek** (`api.deepseek.com`) — generates the broadcast text if DeepSeek is your chosen main AI.
- **ElevenLabs** (`api.elevenlabs.io`) — only if you enable external voice narration, to generate spoken audio from segment text.
- **Stability AI** (`api.stability.ai`) — only if you enable and configure Stability AI images, to generate artwork from an image prompt.
- **Wikipedia** (`wikipedia.org`) — only when no Anthropic key is available, or when the optional fast-preview toggle is on, to fetch a preview thumbnail.
- **Apple** — iCloud (if sync is on) and StoreKit (for the subscription), both under your own Apple ID and governed by Apple's own privacy policy.

We don't share data with anyone else, and we don't sell data — there's no data collected on our end to sell.

## Changes to this policy

If this policy changes, the update will be posted here with a new "Last updated" date.

## Contact

Questions about this policy? Email **tapacuk93@gmail.com** or [open an issue](https://github.com/tapacuk93/infinite-ai-radio-support/issues).
