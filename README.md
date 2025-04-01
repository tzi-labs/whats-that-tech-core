
---![255c0691-b785-467d-95cf-a0a4a35fcf5b](https://github.com/user-attachments/assets/7c804d73-d067-4f04-b439-78ecaa0eefb6)


## 🧠 Detection Strategy

Detection configs (`<tech>.json`) may include:

| Key              | Description |
|------------------|-------------|
| `globalVariables`| Global JS variables (e.g. `window.React`) |
| `requestUrlRegex`| Regex to match URLs of external resources |
| `metaTagCheck`   | Looks for specific `<meta>` tags |
| `selectorExists` | Checks for DOM elements or attributes |
| `htmlRegex`      | Raw HTML pattern matching |
| `themeDetection` | (Optional) Infers themes/templates |

---

## 🧪 Tests

Each technology has two test HTML fixtures:

- `*.pass.html`: Positive detection case
- `*.fail.html`: Negative case

These fixtures help validate detectors and ensure updates don’t introduce false positives or negatives.

Why are the tests made this way, you ask? Well, it's because if we were inputting a URL for a test, then it's possible a framework can change, and the tests will fail in the future or give false positives.

---

## 🔄 Used In

This repo is **not standalone** — it's a submodule of these SDKs:

- [whatsthattech-js-sdk](https://github.com/tzi-labs/whatsthattech-js-sdk)
- (Coming soon) Python SDK, PHP SDK, Go SDK, Rust SDK, etc.

These SDKs handle fetching/parsing HTML. This submodule defines **what to look for**.

---

## 🤝 Contributing

Want to add or improve a tech detector?

> **Do NOT directly PR this repo unless absolutely necessary.**

Instead:

1. **Fork the SDK you’re working with** (e.g. [whatsthattech-js-sdk](https://github.com/tzi-labs/whatsthattech-js-sdk))
2. Modify the `core-logic` Git submodule inside the fork
3. Commit the submodule changes and open a PR on the SDK repo

This ensures changes are integrated and tested across the SDKs that consume this logic.

---

## 📄 License

MIT License  
Copyright © 2025 [tzi-labs](https://github.com/tzi-labs)

---

## ✨ Roadmap

- 🔍 Backend tech detection (Node, PHP, Ruby, Go, Python, Rust)
- 🎯 Confidence scoring & false-positive prevention
- 🌐 Live detection via browser automation (Puppeteer/Playwright)
- 🎨 Theme/plugin detection for CMS (WordPress, Shopify, etc.)

---

## 🛠 Who It's For

Built for:

- Technical SEO experts
- Dev tool makers
- Security researchers
- Growth hackers
- Competitive analysts

Want to know *what's powering a website*?  
**Just ask:** `whatsthattech`.

---
