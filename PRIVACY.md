# Privacy Policy

**Last updated: 2026-07-10**

Infinite AI Radio (iPhone, iPad, and Mac) is designed to collect as little data as possible. This policy explains exactly what the app does and does not do with your information, and applies the same way on every platform.

## Data we don't collect

Infinite AI Radio has no backend server of its own, no user accounts, and no analytics or tracking SDKs. We (the developer) do not receive, store, or have access to your topics, listening history, or API key.

## Your Anthropic API key

The app requires your own Anthropic API key to generate broadcasts. This key is:
- Stored only on your device (locally, never in iCloud or any third-party backup we control).
- Sent only to `api.anthropic.com` over HTTPS, to generate broadcast text and (optionally) look up an image for the current topic.
- Never sent to us or to any other server.

Usage of your key is billed directly by Anthropic to your own account. See [Anthropic's privacy policy](https://www.anthropic.com/legal/privacy) for how they handle that traffic.

## Topics and broadcast content

Whatever topic you type in, and the resulting generated text, is sent to Anthropic's API to produce the broadcast and is processed under Anthropic's own data-handling policies (see link above). This content is not sent anywhere else.

Your station history (the topics you've tuned to and how deep you dove into each) is stored locally on your device only, so it's available across app launches — it is never uploaded anywhere.

## Images

To show a relevant photo alongside a broadcast, the app either:
- Asks Claude to run a web search on your behalf (through the same `api.anthropic.com` connection as above), or
- Fetches a quick preview thumbnail from Wikipedia, if you've enabled the "fast image previews" toggle in Settings.

Either way, only the topic/subject text needed to find a matching photo is sent — never your API key.

## Third parties

The only third parties involved are:
- **Anthropic** (`api.anthropic.com`) — generates the broadcast text and, when relevant, runs image searches.
- **Wikipedia** (`wikipedia.org`) — only when the optional fast-preview toggle is on, to fetch a preview thumbnail.

We don't share data with anyone else, and we don't sell data — there's no data collected on our end to sell.

## Changes to this policy

If this policy changes, the update will be posted here with a new "Last updated" date.

## Contact

Questions about this policy? Email **tapacuk93@gmail.com** or [open an issue](https://github.com/tapacuk93/infinite-ai-radio-support/issues).
