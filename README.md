# Formboost Documentation

Official GitHub documentation for [Formboost](https://formboost.app/), a developer-first form backend for websites.

Formboost lets you receive and manage website form submissions without building or maintaining your own backend infrastructure.

> Canonical documentation: [https://formboost.app/docs](https://formboost.app/docs)
>
> Product website: [https://formboost.app/](https://formboost.app/)

## Quick start

Create a form in the [Formboost dashboard](https://dashboard.formboost.app/) and point your HTML form to your Formboost endpoint:

```html
<form action="https://formboost.app/f/YOUR_ENDPOINT_ID" method="POST">
  <label for="email">Email</label>
  <input id="email" name="email" type="email" required />

  <label for="message">Message</label>
  <textarea id="message" name="message"></textarea>

  <button type="submit">Send</button>
</form>
```

No SDK, API key, JavaScript, or custom server is required for a basic HTML form.

## Documentation

- [Getting Started](./getting-started.md)
- [API Reference & Configuration](./api-reference.md)
- [Integrations](./integrations/README.md)
  - [Discord](./integrations/discord.md)
  - [Slack](./integrations/slack.md)
  - [Telegram](./integrations/telegram.md)
  - [HTTP Webhook](./integrations/http-webhook.md)
  - [Zapier](./integrations/zapier.md)
  - [n8n](./integrations/n8n.md)
  - [Google Sheets](./integrations/google-sheets.md)
- [Framework Guides](./frameworks/README.md)

## Endpoint format

```text
https://formboost.app/f/YOUR_ENDPOINT_ID
```

You can send standard HTML form data or JSON to the same endpoint.

## Useful links

- [Formboost](https://formboost.app/)
- [Documentation](https://formboost.app/docs)
- [Dashboard](https://dashboard.formboost.app/)
- [Integrations](https://formboost.app/integrations)
- [Pricing](https://formboost.app/pricing)
- [Status](https://status.formboost.app/)

## Source of truth

The live documentation at [formboost.app/docs](https://formboost.app/docs) is the canonical product documentation. This repository provides a developer-friendly Markdown version for GitHub discovery, examples, sharing, and contributions.

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md).
