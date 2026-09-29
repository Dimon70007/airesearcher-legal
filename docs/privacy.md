# Privacy Policy

**Last updated:** September 29, 2026  
**App:** AI Researcher (mobile application)  
**Contact:** support email shown in the app Settings

This Privacy Policy describes how the AI Researcher app (“App”, “we”, “us”) handles information when you use our research and summarization features.

## Summary

- **On-device AI:** Summaries and analysis are generated **on your device** using a local language model. We do not receive your generated reports unless you choose to share them.
- **Network use:** The App may send **URLs you submit** and related metadata to third-party services to fetch page content or video captions before local analysis.
- **Local storage:** Research history and settings are stored **on your device**.
- **Ads (free tier):** In the current MVP for Russia / RuStore, ads are served by **Yandex Mobile Ads**. Advertising SDKs may collect advertising identifiers and device signals as described below.
- **Analytics & crashes:** We use **Yandex AppMetrica** for ad-funnel analytics (when enabled) and for **crash / error reporting** (stack traces, device diagnostics) so we can fix stability issues.
- **Premium (early):** Paid Premium, where offered, is processed via **web checkout (Robokassa)** and a billing backend. Native store billing (Google Play / Apple / RuStore Pay / RevenueCat) may be added later and is not required for the current MVP.

## Information we process

### Information you provide

- **URLs** (web pages, YouTube links, etc.) that you enter for research.
- **Optional follow-up questions** about a research report (processed on-device).
- **App settings** (e.g. summary language preference), stored locally.

### Information collected automatically

- **Device and app diagnostics / crash reports** via **Yandex AppMetrica Crashes** (and similar OS tools): crash stack traces, error messages, and basic device/app metadata. This does **not** include your research URLs, report text, or other content you analyze.
- **Subscription / entitlement status** if you purchase Premium (early: Robokassa + billing backend; later: app stores / RevenueCat if enabled).
- **Advertising identifiers** (e.g. Google Advertising ID / IDFA where applicable) and related device signals when ads are shown, primarily via **Yandex Mobile Ads**. Other networks (e.g. Google AdMob) may be added in a later release and will be disclosed here before use.
- **Ads conversion analytics (when remote analytics is enabled):** anonymized ad funnel events (`ad_request` / fill / impression / fail) may be sent to **Yandex AppMetrica** for Yandex ad activity. **Google Firebase Analytics** for non-Yandex networks is **not** used in the current MVP and may be added later if those networks ship. These events do not include research URLs, report text, or other content you analyze. See also in-app Settings → Privacy & Ads.

We do **not** require account registration for core App features.

## How we use information

| Data | Purpose |
|------|---------|
| URLs you submit | Fetch source text or captions for analysis |
| Source text (transient) | Input to the on-device model to produce your report |
| Research reports | Stored locally in your research history |
| Settings | Personalize language and app behavior |
| Advertising identifiers / SDK signals | Serve and measure ads (free tier); respect OS privacy / consent where required |
| AppMetrica crash / error reports | Diagnose crashes and improve App stability |
| Subscription / payment metadata | Grant and renew Premium; disable ads while Premium is active |

We do **not** sell your personal information.

## Third-party services

The App may contact:

1. **Yandex Mobile Ads** — to show ads to free users (current MVP / Russia path). May process advertising identifiers and related signals under Yandex policies.
2. **Yandex AppMetrica** — ad-funnel analytics (when enabled) and **crash reporting** (stack traces / diagnostics). Policy: [https://yandex.com/legal/metrica_termsofuse/](https://yandex.com/legal/metrica_termsofuse/)
3. **YouTube caption proxy** (self-hosted) — to retrieve public video captions for URLs you provide. Only the video URL and language preference are sent. The same proxy may forward content-extract/search requests to Tavily on your behalf.
4. **Tavily** (or similar) — to extract or search web content from URLs you provide. On the mobile App this is typically reached **through our self-hosted caption/proxy server**, which then calls Tavily. Their policy: [https://tavily.com](https://tavily.com)
5. **Model CDN / model hosting** — to download the on-device AI model file to your phone.
6. **Robokassa** (or similar web payment provider) — if you complete Premium checkout on the web (early Premium path; not used as an App Store IAP substitute on iOS unless Apple-allowed programs apply).
7. **Billing backend** (our server) — anonymous app user id, plan, and entitlement expiry for web Premium.
8. **May be added later (not current MVP):** Google AdMob or other global ad networks; Google Firebase Analytics for those networks’ conversion events; Google Play Billing / Apple In-App Purchase / RuStore Billing / RevenueCat for store subscriptions.

Each third party processes data under its own privacy policy. We recommend reviewing those policies.

## Ads and Premium

- Free users may see ads in limited placements (e.g. Home banner, research loading). Ads are not shown on the model setup flow or during active on-device generation streaming.
- While **Premium** is active, ads are disabled.
- You can review privacy / ads settings in the App where provided (e.g. consent forms required by law in your region).

## Data storage and retention

- **On device:** Research history (SQLite), preferences (local storage), downloaded AI model files, cached Premium entitlement / expiry.
- **On our servers:** We do not operate a general user-account backend for the MVP App. Caption / Tavily-proxy logs, if any, should be limited to operational troubleshooting. **Billing backend** (web payments) may store an anonymous app user id, plan, and entitlement expiry needed to grant/revoke Premium.
- **AppMetrica / advertising partners** retain analytics and crash data per their policies and applicable law.

You can **clear research history** in App Settings. Ending Premium follows store or web-provider cancel/refund rules; after expiry or revoke, ads may return.

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
