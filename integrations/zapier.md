# Zapier Integration

Connect [Formboost](https://formboost.app/) submissions to Zapier so new form entries can trigger workflows across other apps.

## Typical flow

```text
Website form -> Formboost -> Zapier -> CRM / Email / Sheets / Other apps
```

## Setup

1. Create or open a form in the [Formboost dashboard](https://dashboard.formboost.app/).
2. Open **Integrations** and choose **Zapier**.
3. Follow the connection instructions shown in Formboost.
4. In Zapier, create a Zap using the Formboost submission trigger or the connection method described in the dashboard.
5. Map the submitted fields to your destination action.
6. Send a test submission.

Your frontend endpoint stays the same:

```text
https://formboost.app/f/YOUR_ENDPOINT_ID
```

For current Zapier setup details, use the canonical [Formboost documentation](https://formboost.app/docs).
