# n8n Integration

Use [Formboost](https://formboost.app/) with n8n to automate workflows from new form submissions.

## Typical flow

```text
Website form -> Formboost -> n8n -> Database / CRM / Email / Internal API
```

## Setup

1. Open your form in the [Formboost dashboard](https://dashboard.formboost.app/).
2. Open **Integrations** and choose **n8n**.
3. Configure the webhook or connection details shown by Formboost.
4. Build your n8n workflow and map the submitted fields.
5. Send a test submission and verify the workflow runs.

Your site continues submitting to:

```text
https://formboost.app/f/YOUR_ENDPOINT_ID
```

Treat submission fields as untrusted input and validate before storing or forwarding them.

For the latest configuration, see the [official Formboost documentation](https://formboost.app/docs).
