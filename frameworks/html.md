# HTML + Formboost

Connect a plain HTML form to [Formboost](https://formboost.app/) with only an `action` and `method`.

```html
<form action="https://formboost.app/f/YOUR_ENDPOINT_ID" method="POST">
  <input type="text" name="name" required />
  <input type="email" name="email" required />
  <textarea name="message"></textarea>
  <button type="submit">Send</button>
</form>
```

Replace `YOUR_ENDPOINT_ID` with your actual endpoint from the [Formboost dashboard](https://dashboard.formboost.app/).

## Optional redirect

```html
<input type="hidden" name="_redirect" value="https://example.com/thank-you" />
```

## Optional honeypot

```html
<input type="text" name="_honey" style="display:none" tabindex="-1" autocomplete="off" />
```

See the [official Formboost docs](https://formboost.app/docs) for current configuration options.
