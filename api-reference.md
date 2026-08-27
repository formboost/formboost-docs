# Formboost API Reference

Canonical reference: [https://formboost.app/docs/api](https://formboost.app/docs/api)

## Submission endpoint

Send submissions to:

```text
POST https://formboost.app/f/YOUR_ENDPOINT_ID
```

Formboost accepts regular browser form submissions and JSON requests.

## HTML form submission

```html
<form action="https://formboost.app/f/YOUR_ENDPOINT_ID" method="POST">
  <input name="name" />
  <input name="email" type="email" />
  <textarea name="message"></textarea>
  <button type="submit">Submit</button>
</form>
```

## JSON submission

```bash
curl -X POST "https://formboost.app/f/YOUR_ENDPOINT_ID" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "Jane Doe",
    "email": "jane@example.com",
    "message": "Hello"
  }'
```

## Built-in fields

### `_redirect`

Redirect the browser after a successful HTML form submission.

```html
<input type="hidden" name="_redirect" value="https://example.com/thank-you" />
```

The redirect URL should use HTTPS.

### `_honey`

Add a hidden honeypot field for basic bot detection.

```html
<input type="text" name="_honey" style="display:none" tabindex="-1" autocomplete="off" />
```

Legitimate users should leave this field empty.

## Webhook event shape

Webhook integrations receive structured form submission events. A typical payload looks like:

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

Form IDs are not exposed in the public webhook payload.

## CORS and browser requests

When using JavaScript, submit requests directly to the public Formboost endpoint. For normal HTML forms, use the form `action` attribute instead of JavaScript whenever possible.

## Related documentation

- [Getting Started](./getting-started.md)
- [HTTP Webhook](./integrations/http-webhook.md)
- [Formboost documentation](https://formboost.app/docs)
- [Formboost website](https://formboost.app/)
