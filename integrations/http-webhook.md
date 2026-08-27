# HTTP Webhook Integration

Use Formboost HTTP webhooks to forward form submissions to your own API, automation service, CRM, or internal system.

Product: [https://formboost.app/](https://formboost.app/)

## Configure the webhook

1. Open your form in the [Formboost dashboard](https://dashboard.formboost.app/).
2. Open **Integrations**.
3. Choose **HTTP Webhook**.
4. Enter your HTTPS webhook URL.
5. Save the integration and send a test submission.

## Example event

```json
{
  "eventId": "sub_3b241101-e2bb-4255-8caf-4136c566a962",
  "event": "form.submission",
  "sentAt": "2026-08-23T12:00:00.000Z",
  "form": {
    "name": "Contact Form",
    "alias": "contact"
  },
  "submission": {
    "submitted_at": "2026-08-23T12:00:00.000Z",
    "name": "John Doe",
    "email": "john@example.com",
    "message": "Hello"
  }
}
```

## Example Express receiver

```js
import express from 'express';

const app = express();
app.use(express.json());

app.post('/formboost-webhook', async (req, res) => {
  const event = req.body;

  if (event.event === 'form.submission') {
    console.log('Form:', event.form?.name);
    console.log('Submission:', event.submission);
  }

  res.sendStatus(200);
});

app.listen(3000);
```

Return a successful `2xx` response after accepting the event.

## Security recommendations

- Always use HTTPS.
- Treat submitted form values as untrusted input.
- Validate data before storing or processing it.
- Do not log sensitive customer submission data unnecessarily.
- Keep secrets and internal credentials out of webhook URLs.

See the [Formboost documentation](https://formboost.app/docs) for current behavior and integration settings.
