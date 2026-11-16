# Nova Revival

A mobile-first health dashboard that runs entirely in the browser. It has a period cycle tracker, a wellness score, daily tasks and an optional AI assistant that can explain a photo of a health report.



<!-- Add 2 or 3 screenshots here -->

## Features

- **Cycle tracker:** enter the first day of your last period, your cycle length and your period length. The app shows a ring with the four phases, today's cycle day, days until the next period and an estimated fertile window. Everything is saved on your device.
- **Wellness dashboard:** live heart-rate chart, wellness score, stress level and a weekly history chart.
- **Daily tasks:** small wellness tasks that earn points and reset every day.
- **Assistant:** answers common health questions with simple built-in keyword replies. It also answers questions about your current cycle phase.
- **Optional AI mode:** paste your own API key in Settings to get free-form answers and report scanning.
- **Report scanning:** take or upload a photo (PNG, JPG or WebP) of a lab or health report and get a plain-language explanation.
- English and Hindi, dark and light themes, and a layout built for phones.

## AI setup (bring your own key)

The app has no server and no key of its own. Each user pastes their own API key in Settings.

Supported providers: Claude (Anthropic), OpenAI, Gemini (Google), OpenRouter, and any OpenAI-compatible service through the "Other" option with a base URL. The provider is detected from the key's prefix, or you can pick it by hand. You can also type a model name. Report scanning needs a model that can read images.

- Your key is stored only in your browser's local storage and is sent only to the provider you chose.
- Only your question and your cycle day and phase are sent. Your name and exact dates are never sent.
- A report photo goes to your chosen provider. Crop out your name and ID before scanning.
- Anyone using the same browser can use the saved key. Remove it on shared devices, and set a spending limit with your provider.
- Some providers block calls made directly from a browser. Those will not work.

## Privacy

There is no backend, no account and no analytics. Cycle data, tasks and settings live in your browser's local storage. Logging out clears them.

## Limitations

- **Heart rate, oxygen, steps and sleep are simulated.** They are demo values, not real measurements. This is not connected to any sensor or wearable.
- **Cycle dates are estimates.** Ovulation is assumed to happen about 14 days before the next period, so the fertile window is approximate. It is not contraception and not medical advice.
- Without an API key, the assistant uses simple keyword matching. It is not an AI.
- AI answers can be wrong. They are not a diagnosis. Talk to a doctor about your results.
- The charts load Chart.js from a CDN, so they need an internet connection.

## Tech

A single `index.html` file with vanilla JavaScript and CSS. Chart.js 4 is loaded from cdnjs. No build step and no dependencies to install.

## Run it

Open `index.html` in a browser, or turn on GitHub Pages for the repo (Settings, then Pages, then the `main` branch).

## How it was built

This project was built with AI assistance (Claude). The original idea, [what you designed, tested and decided yourself] came from me. Edit this section so it describes your real contribution.

## License

MIT, or add the licence of your choice.
