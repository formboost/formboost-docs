# React + Formboost

Use [Formboost](https://formboost.app/) from React with either a normal HTML form or `fetch`.

## Simple form

```jsx
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

## Submit with fetch

```jsx
async function submitForm(event) {
  event.preventDefault();

  const form = new FormData(event.currentTarget);

  await fetch('https://formboost.app/f/YOUR_ENDPOINT_ID', {
    method: 'POST',
    body: form
  });
}
```

Replace `YOUR_ENDPOINT_ID` with the endpoint from your [Formboost dashboard](https://dashboard.formboost.app/).

For the latest React guidance, see the [official Formboost documentation](https://formboost.app/docs).
