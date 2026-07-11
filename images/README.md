# Images

Screenshots and diagrams for the docs live here, organized by section to match
the paths used in `<Frame>` blocks:

```
images/
  getting-started/
  providers/
  compliance/
  contacts/
  campaigns/
  ...
```

A page references an image like:

```mdx
<Frame caption="Settings → Channels">
  <img src="/images/providers/twilio-connect.png" alt="Connecting Twilio" />
</Frame>
```

Guidelines:

- Capture at 2x (retina) and export as PNG or WebP.
- Crop to the relevant UI; avoid full-screen captures with browser chrome.
- Redact real customer data, phone numbers, and API keys.
- Keep filenames kebab-case and descriptive.
