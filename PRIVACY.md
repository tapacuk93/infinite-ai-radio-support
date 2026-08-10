# Privacy Policy

**Last updated: 2026-08-08**

Infinite AI Radio (iPhone, iPad, and Mac) is designed to collect as little data as possible. This policy explains exactly what the app does and does not do with your information, and applies the same way on every platform.

## Data we don't collect

Infinite AI Radio has no user accounts and no analytics or tracking SDKs. We (the developer) do not receive, store, or have access to your topics or listening history.

## How AI requests work (no personal API keys)

The app does **not** ask you for your own AI provider API key. Instead, every request to generate broadcast text, narration audio, or artwork is sent to our own relay server, **aicoin-proxy**, at `proxy.aicoin.oeaio.com`. aicoin-proxy adds its own paid credential for whichever AI provider the request is for, forwards your request unchanged, and returns the response — you never handle or expose a provider credential, and we never see one of yours because there isn't one.

**1 AICoin = 1 AI API call.** Each broadcast segment, narration clip, or generated image costs exactly 1 AICoin, debited from your AICoin wallet at the moment of the call. In Settings, you pick which AI narrates the broadcast — Claude (Anthropic), OpenAI, or Gemini (Google) — and can optionally enable ElevenLabs narration and/or OpenAI or Stability AI image generation; all of these are billed the same way, 1 AICoin per call, through the same relay.

## AICoin wallet

Your wallet is identified by a keypair generated and stored on your device (Keychain) — we never see your private key. There are two ways to get AICoin:
- **Buy it**, via an in-app purchase processed entirely by Apple through StoreKit. We never see or store your payment details — Apple handles billing and receipts directly. A successful purchase credits your wallet by contacting `proxy.aicoin.oeaio.com` with Apple's own signed proof of purchase.
- **Receive a transfer** from another AICoin wallet (yours on another device, or someone else's).

Your wallet address and balance are stored server-side at `proxy.aicoin.oeaio.com` (see the [aicoin.oeaio.com](https://aicoin.oeaio.com) site for how the ledger works) — this is necessary for the wallet to function across devices and to debit calls, and is not linked to your name, email, or Apple ID.

## Topics and broadcast content

Whatever topic you type in, and the resulting generated text, is sent — via the aicoin-proxy relay described above — to whichever AI provider you've selected as your main narrator, and is processed under that provider's own data-handling policy:
- [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy)
- [OpenAI's privacy policy](https://openai.com/privacy)
- [Google's privacy policy](https://policies.google.com/privacy)
- [ElevenLabs' privacy policy](https://elevenlabs.io/privacy)
- [Stability AI's privacy policy](https://stability.ai/privacy-policy)

If you've turned on ElevenLabs narration and/or DALL-E or Stability AI images in Settings, the segment text or image prompt is also relayed the same way to generate the voice audio or artwork. This content is never sent anywhere else.

Your station history (the topics you've tuned to, how deep you dove into each, and any facts you've saved) is stored locally on your device, so it's available across app launches. If iCloud sync is turned on (Settings, on by default), this history and your app preferences are also synced through your own iCloud account so they carry over to your other devices. This data is only ever accessible to you, through your own iCloud account; we have no access to it.

## Images

To show a relevant photo alongside a broadcast, the app either:
- Asks Claude to run a web search on your behalf (via the relay) whenever Claude is available, or
- Fetches a quick preview thumbnail from Wikipedia (or if you've enabled the "fast image previews" toggle in Settings), or
- Generates an image via OpenAI's DALL-E or Stability AI's API (via the relay), if you've enabled one in Settings.

Either way, only the topic/subject text needed to find or generate a matching photo is sent.

## Third parties

The only third parties involved are:
- **aicoin-proxy** (`proxy.aicoin.oeaio.com`, operated by us) — relays every AI request below with its own paid credentials and debits your wallet; see [aicoin.oeaio.com](https://aicoin.oeaio.com) for how it works.
- **Anthropic** — generates the broadcast text if Claude is your chosen main AI, and runs image searches when available.
- **OpenAI** — generates the broadcast text if OpenAI is your chosen main AI, and/or generates artwork if you enable DALL-E images.
- **Google** — generates the broadcast text if Gemini is your chosen main AI.
- **ElevenLabs** — only if you enable external voice narration, to generate spoken audio from segment text.
- **Stability AI** — only if you enable Stability AI images, to generate artwork from an image prompt.
- **Wikipedia** (`wikipedia.org`) — only when the optional fast-preview toggle is on, or Claude is unavailable, to fetch a preview thumbnail.
- **Apple** — iCloud (if sync is on) and StoreKit (for AICoin purchases), both under your own Apple ID and governed by Apple's own privacy policy.

We don't share data with anyone else, and we don't sell data — there's no data collected on our end to sell.

## Changes to this policy

If this policy changes, the update will be posted here with a new "Last updated" date.

## Contact

Questions about this policy? Email **tapacuk93@gmail.com** or [open an issue](https://github.com/tapacuk93/infinite-ai-radio-support/issues).
