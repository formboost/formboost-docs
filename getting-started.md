# Getting Started with Formboost

[Formboost](https://formboost.app/) is a developer-first form backend that receives and manages form submissions for your website without requiring you to build a custom backend.

Canonical guide: [https://formboost.app/docs/getting-started](https://formboost.app/docs/getting-started)

## 1. Create a Formboost account

Open the [Formboost dashboard](https://dashboard.formboost.app/) and create your account.

## 2. Create a form

Create a new form in the dashboard. Formboost gives the form a public submission endpoint in this format:

```text
https://formboost.app/f/YOUR_ENDPOINT_ID
```

## 3. Connect your website form

```html
<form action="https://formboost.app/f/YOUR_ENDPOINT_ID" method="POST">
  <input type="text" name="name" placeholder="Your name" required />
  <input type="email" name="email" placeholder="you@example.com" required />
  <textarea name="message" placeholder="How can we help?"></textarea>
  <button type="submit">Send message</button>
</form>
```

Replace `YOUR_ENDPOINT_ID` with the endpoint shown in your Formboost dashboard.

## 4. Submit and verify

Submit the form from your website and open the Formboost dashboard. The submission should appear under the form you created.

## Redirect after submission

For traditional browser forms, you can send `_redirect` to control where the visitor goes after a successful submission.

```html
<input type="hidden" name="_redirect" value="https://example.com/thank-you" />
```

Use an HTTPS URL.

## Honeypot field

Formboost supports the `_honey` field as a honeypot for basic bot filtering.

```html
<input type="text" name="_honey" style="display:none" tabindex="-1" autocomplete="off" />
```

Keep the field empty for legitimate visitors.

## JavaScript / JSON example

```js
await fetch('https://formboost.app/f/YOUR_ENDPOINT_ID', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    name: 'Jane Doe',
    email: 'jane@example.com',
    message: 'Hello from my website'
  })
});
```

## Next steps

- Read the [API Reference](./api-reference.md)
- Configure [Integrations](./integrations/README.md)
- Follow a [Framework Guide](./frameworks/README.md)
- Browse the canonical [Formboost documentation](https://formboost.app/docs)
