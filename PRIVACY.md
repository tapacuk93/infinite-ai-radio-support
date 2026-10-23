# Privacy Policy

**Last updated: 2026-10-23**

Infinite AI Radio (iPhone, iPad, and Mac) is designed to collect as little data as possible. This policy explains exactly what the app does and does not do with your information, and applies the same way on every platform.

## Data we don't collect

Infinite AI Radio has no user accounts and no analytics or tracking SDKs. We (the developer) do not receive, store, or have access to your topics or listening history.

## How AI requests work (no personal API keys)

The app does **not** ask you for your own AI provider API key. Instead, every request to generate broadcast text, narration audio, or artwork is sent to our own relay server, **aicoin-proxy**, at `proxy.aicoin.oeaio.com`. aicoin-proxy adds its own paid credential for whichever AI provider the request is for, forwards your request to that provider, and returns the response — you never handle or expose a provider credential, and we never see one of yours because there isn't one.

**AI calls are paid for in AICoin, priced by what they cost to run.** Each broadcast segment, narration clip, or generated image costs from 1 AICoin — a short call costs one, a longer one costs more, because a longer segment genuinely costs more to generate. The charge is worked out from the provider's own usage figures for that call and debited from your wallet at the moment of the call; the relay reports it back to the app, so what you were charged is never hidden from you. In Settings, you pick which AI writes the broadcast — Claude (Anthropic), OpenAI, Gemini (Google), Mistral, Kimi (Moonshot AI), or Automatic, which lets the relay pick one of them — and whether to use ElevenLabs narration and OpenAI or Stability AI image generation (both on by default, and both can be turned off); all of these are billed the same way, per call and by cost, through the same relay.

### The provider credential is shared by everyone

There is one relay account per AI provider, and every user's requests go through it. To the provider, all of this app's traffic looks like a single customer — ours — rather than like you.

That has consequences worth stating plainly:

- **Your usage affects other listeners.** Rate limits, quotas, and spending caps apply to the shared credential as a whole. Heavy use, or a burst of requests, can slow down or temporarily block generation for everyone using the app, not just for you.
- **So does what you type.** Providers enforce their own usage policies at the account level. Content that trips a provider's safety systems is attributed to the shared credential, and repeated violations can get that credential rate-limited, restricted, or suspended — which would stop the app working for every user until it is resolved. Please don't send anything you wouldn't want charged to a shared account.
- **Provider-side features are account-scoped.** Anything a provider does per account rather than per end user — abuse scoring, caching, aggregate logging — covers all of this app's traffic together.

What this does **not** mean: your topics and generated segments are not pooled, mixed into other people's broadcasts, or shown to other users by the app. Each broadcast is generated from your own request and returned only to your device. The sharing described here is of the provider *account*, not of your content.

### What the relay keeps, and what the providers keep

- **The relay does not log or store what you send or get back** — no topics, prompts, segment text, audio, or images. For each request it keeps only a line of metadata: the time, the kind of request and the provider's endpoint (without query parameters; for narration this includes the ID of the voice used), which provider, your wallet address, the result status, sizes, timings, and the AICoin charged. Those logs rotate and are capped in size.
- **The AI providers do receive your requests**, and keep them under their own retention policies (linked below) — the same as for any other customer of theirs.
- **Nothing you send is stored on a provider where other users could reach it.** Because the provider account is shared, the relay only forwards requests to providers' generation endpoints, and refuses the provider features that store things on the account — file uploads, batch jobs, stored responses and conversations, caches, and generation history. For OpenAI it also switches off response storage on every request.
- **The one exception is designed voices.** In the default "Match to content" voice mode, the app has Claude write a short voice description from your station's topic and asks ElevenLabs to design a voice from it; that voice is saved in the shared ElevenLabs account under a name like "Auto: *your topic*". The relay records which wallet created each voice: only your wallet sees it in voice lists and only your wallet can delete it. The app keeps at most five such voices and deletes the oldest as it makes new ones; voices you design yourself in Settings stay until you delete them.

## AICoin wallet

Your wallet is identified by a keypair generated and stored on your device (Keychain) — we never see your private key. There are two ways to get AICoin:
- **Buy it**, via an in-app purchase processed entirely by Apple through StoreKit. We never see or store your payment details — Apple handles billing and receipts directly. A successful purchase credits your wallet by contacting `proxy.aicoin.oeaio.com` with Apple's own signed proof of purchase.
- **Receive a transfer** from another AICoin wallet (yours on another device, or someone else's). Sending and receiving is not offered inside the app; it happens through the web wallet at [aicoin.oeaio.com](https://aicoin.oeaio.com), and coins arriving that way are credited to the same wallet address the app uses.

Your wallet address and balance are stored server-side at `proxy.aicoin.oeaio.com` (see the [aicoin.oeaio.com](https://aicoin.oeaio.com) site for how the ledger works) — this is necessary for the wallet to function across devices and to debit calls, and is not linked to your name, email, or Apple ID.

## Topics and broadcast content

Whatever topic you type in, and the resulting generated text, is sent — via the aicoin-proxy relay described above — to whichever AI provider you've selected (if that provider fails, the request may be retried with another of the providers listed here), and is processed under that provider's own data-handling policy:
- [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy)
- [OpenAI's privacy policy](https://openai.com/privacy)
- [Google's privacy policy](https://policies.google.com/privacy)
- [Mistral AI's privacy policy](https://mistral.ai/terms#privacy-policy)
- [Moonshot AI's (Kimi) privacy policy](https://platform.moonshot.ai/docs/agreement/userprivacy)
- [ElevenLabs' privacy policy](https://elevenlabs.io/privacy)
- [Stability AI's privacy policy](https://stability.ai/privacy-policy)

While ElevenLabs narration and AI images are on (the default), the segment text or image prompt is also relayed the same way to generate the voice audio or artwork, and a voice description is relayed to ElevenLabs to design a station voice (see "What the relay keeps" above). This content is never sent anywhere else.

Your station history (the topics you've tuned to, how deep you dove into each, and any facts you've saved) is stored locally on your device, so it's available across app launches. If iCloud sync is turned on (Settings, on by default), this history and your app preferences are also synced through your own iCloud account so they carry over to your other devices. This data is only ever accessible to you, through your own iCloud account; we have no access to it.

## Images

To show a relevant photo alongside a broadcast, the app either:
- Asks Claude to run a web search on your behalf (via the relay) whenever Claude is available, or
- Fetches a quick preview thumbnail from Wikipedia (or if you've enabled the "fast image previews" toggle in Settings), or
- Generates an image via OpenAI's DALL-E or Stability AI's API (via the relay), while AI images are on in Settings (the default). Each station's backdrop is also painted by Stability AI from a description Claude writes.

Either way, only the topic/subject text needed to find or generate a matching photo is sent.

## Third parties

The only third parties involved are:
- **aicoin-proxy** (`proxy.aicoin.oeaio.com`, operated by us) — relays every AI request below with its own paid credentials and debits your wallet; see [aicoin.oeaio.com](https://aicoin.oeaio.com) for how it works.
- **Anthropic** — generates the broadcast text if Claude is your chosen AI, and runs image searches, station designs and voice descriptions when available.
- **OpenAI** — generates the broadcast text if OpenAI is your chosen AI, and generates artwork while AI images are on.
- **Google** — generates the broadcast text if Gemini is your chosen AI.
- **Mistral** and **Moonshot AI (Kimi)** — generate the broadcast text if you choose one of them, or if Automatic picks one.
- **ElevenLabs** — while external voice narration is on (the default), to generate spoken audio from segment text and to design station voices.
- **Stability AI** — while AI images are on (the default), to generate artwork and station backdrops from an image prompt.
- **Wikipedia** (`wikipedia.org`) — only when the optional fast-preview toggle is on, or Claude is unavailable, to fetch a preview thumbnail.
- **Apple** — iCloud (if sync is on) and StoreKit (for AICoin purchases), both under your own Apple ID and governed by Apple's own privacy policy.

We don't share data with anyone else, and we don't sell data — there's no data collected on our end to sell.

## Changes to this policy

If this policy changes, the update will be posted here with a new "Last updated" date.

## Contact

Questions about this policy? Email **tapacuk93@gmail.com** or [open an issue](https://github.com/tapacuk93/infinite-ai-radio-support/issues).
