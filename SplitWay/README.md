# SplitWay 🧾

**AI-Powered Bill Splitting — Scan a receipt, assign items, send payment requests.**

SplitWay is a mobile-first web app that eliminates the awkwardness of splitting restaurant bills. Snap a photo of your receipt, let AI read it, assign each item to whoever ordered it, and send everyone a text or payment request with their exact amount owed.

![Status](https://img.shields.io/badge/Status-Live-brightgreen)
![License](https://img.shields.io/badge/License-MIT-blue)
![Built With](https://img.shields.io/badge/Built%20With-Vanilla%20JS-yellow)

---

### Technical Highlights
- **Claude Vision API** for accurate receipt OCR and structured data extraction
- **Surgical DOM updates** — only the changed row re-renders on assignment, zero flicker
- **localStorage** for cross-session contact memory
- **Camera API** with rear-camera preference and gallery upload fallback
- Zero dependencies — pure HTML, CSS, vanilla JavaScript
- Single `index.html` file — deploy anywhere static hosting works

---

## 📱 How to Use

1. **Who's dining?** Add friends by name + phone, or hit **+ Add Random Group** to demo
2. **Who paid?** Tap the person who covered the check
3. **Scan receipt** — take a photo or upload; AI extracts all items automatically
4. **Assign items** — use the dropdown on each row; items turn green when assigned
5. **Adjust tip** — use the slider, preset buttons, or type a custom amount
6. **Calculate & send** — review the split summary, then tap **Send Text Requests**

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| AI / OCR | Claude Vision API (claude-sonnet-4-5) |
| Camera | MediaDevices Web API |
| Storage | Browser localStorage |
| Hosting | GitHub Pages (static) |
| Messaging | SMS URL scheme (`sms:`) |

---

# Python
python -m http.server 8000



> **Note:** The Claude Vision receipt scanning requires network access to `api.anthropic.com`. This works automatically on GitHub Pages (HTTPS). Locally, the app falls back gracefully if the API is unreachable.

---


> Built as a portfolio project demonstrating AI-native product thinking, mobile web development, and real-world UX design for the commerce/payments space.
