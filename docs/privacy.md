# Privacy Policy

**Last updated:** July 5, 2026  
**App:** AI Researcher (mobile application)  
**Contact:** support email shown in the app Settings

This Privacy Policy describes how the AI Researcher app (“App”, “we”, “us”) handles information when you use our research and summarization features.

## Summary

- **On-device AI:** Summaries and analysis are generated **on your device** using a local language model. We do not receive your generated reports unless you choose to share them.
- **Network use:** The App may send **URLs you submit** and related metadata to third-party services to fetch page content or video captions before local analysis.
- **Local storage:** Research history and settings are stored **on your device**.

## Information we process

### Information you provide

- **URLs** (web pages, YouTube links, etc.) that you enter for research.
- **Optional follow-up questions** about a research report (processed on-device).
- **App settings** (e.g. summary language preference), stored locally.

### Information collected automatically

- **Device and app diagnostics** that the operating system or crash reporting tools may collect (standard for mobile apps).
- **Subscription status** if you use in-app purchases (processed by Google Play / Apple App Store and our subscription provider, e.g. RevenueCat).

We do **not** require account registration for core App features.

## How we use information

| Data | Purpose |
|------|---------|
| URLs you submit | Fetch source text or captions for analysis |
| Source text (transient) | Input to the on-device model to produce your report |
| Research reports | Stored locally in your research history |
| Settings | Personalize language and app behavior |

We do **not** sell your personal information.

## Third-party services

The App may contact:

1. **Tavily** (or similar) — to extract or search web content from URLs you provide. Their policy: [https://tavily.com](https://tavily.com)
2. **YouTube caption proxy** (self-hosted or cloud worker) — to retrieve public video captions for URLs you provide. Only the video URL and language preference are sent.
3. **Model CDN** — to download the on-device AI model file to your phone.
4. **RevenueCat / Google Play Billing** — if you purchase a subscription.

Each third party processes data under its own privacy policy. We recommend reviewing those policies.

## Data storage and retention

- **On device:** Research history (SQLite), preferences (local storage), downloaded AI model files.
- **On our servers:** We do not operate a user account backend for the MVP App. Caption proxy logs, if any, should be limited to operational troubleshooting; avoid submitting sensitive URLs if concerned.

You can **clear research history** in App Settings.

## Data security

- Analysis runs locally after source material is fetched.
- API keys for third-party services are embedded in the App build or developer configuration; they are not your personal credentials.
- HTTPS is used for remote caption and content APIs where configured.

No method of transmission or storage is 100% secure.

## Children’s privacy

The App is not directed at children under 13. We do not knowingly collect personal information from children.

## Your rights

Depending on your region, you may have rights to access, delete, or restrict processing of personal data. For requests, contact us at the support email in Settings.

## International transfers

Third-party providers may process data in countries other than yours.

## Changes

We may update this Privacy Policy. The “Last updated” date will change. Continued use of the App after changes means you accept the updated policy.

## Contact

Questions about this Privacy Policy: use the **support email** shown in the App Settings screen.
