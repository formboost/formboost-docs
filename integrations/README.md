# Formboost Integrations

Connect [Formboost](https://formboost.app/) form submissions to the tools your team already uses.

Canonical integrations documentation: [https://formboost.app/docs/integrations](https://formboost.app/docs/integrations)

## Available integrations

- [Discord](./discord.md)
- [Slack](./slack.md)
- [Telegram](./telegram.md)
- [HTTP Webhook](./http-webhook.md)
- [Zapier](./zapier.md)
- [n8n](./n8n.md)
- [Google Sheets](./google-sheets.md)

## How integrations work

1. Create a form in the [Formboost dashboard](https://dashboard.formboost.app/).
2. Open the form's integration settings.
3. Configure the destination.
4. Submit a test form.
5. Confirm the integration receives the event.

Your website continues posting submissions to:

```text
https://formboost.app/f/YOUR_ENDPOINT_ID
```

Integrations run after Formboost receives the submission, so your frontend does not need separate integration-specific code.

For current product details, visit the [Formboost integrations page](https://formboost.app/integrations) or [official docs](https://formboost.app/docs).
