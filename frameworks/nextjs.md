# Next.js + Formboost

Use [Formboost](https://formboost.app/) directly from a Next.js client form without creating a custom API route.

```tsx
'use client';

export default function ContactForm() {
  return (
    <form action="https://formboost.app/f/YOUR_ENDPOINT_ID" method="POST">
      <input name="name" placeholder="Name" required />
      <input name="email" type="email" placeholder="Email" required />
      <textarea name="message" placeholder="Message" />
      <button type="submit">Send</button>
    </form>
  );
}
```

Replace `YOUR_ENDPOINT_ID` with the endpoint from your [Formboost dashboard](https://dashboard.formboost.app/).

If you need a fully custom UX, submit to the same endpoint with `fetch` from a client component.

For the latest Next.js guidance, see the [official Formboost documentation](https://formboost.app/docs).
