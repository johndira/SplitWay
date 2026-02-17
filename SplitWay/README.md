# SplitWay 🧾

**AI-Powered Bill Splitting — Scan a receipt, assign items, send payment requests.**

SplitWay is a mobile-first web app that eliminates the awkwardness of splitting restaurant bills. Snap a photo of your receipt, let AI read it, assign each item to whoever ordered it, and send everyone a text with their exact amount owed.

![Status](https://img.shields.io/badge/Status-Live-brightgreen)
![License](https://img.shields.io/badge/License-MIT-blue)
![Built With](https://img.shields.io/badge/Built%20With-Vanilla%20JS-yellow)

---

## 🌟 Features

### Core Flow
- **Add your group** — enter names + phone numbers manually, or tap **+ Add Random Group** to instantly populate a demo group and try the full flow
- **Saved contacts** — anyone you've added manually is remembered and offered as quick-tap chips on your next visit (via localStorage)
- **Select the payer** — choose who covered the bill upfront
- **Scan the receipt** — use your device camera or upload from your gallery
- **AI receipt parsing** — Claude Vision reads item names, quantities, prices, tax, and any extra fees automatically
- **Quantity expansion** — if a receipt shows `2 Fried Chicken Sandwich $18.00`, SplitWay creates two separate $9.00 assignment rows, one per sandwich
- **Assign items** — dropdown per item: assign to one person, split among all, or pick a custom subset
- **Custom split** — tap "Split – Custom" to choose exactly which people share an item (e.g. 2 of 5 people split an appetizer)
- **Adjustable tip** — slider (0–40%), preset buttons (15% / 18% / 20% / 25%), or type a custom dollar amount
- **Live updates** — assigned rows turn green instantly, names appear below each item, tip row updates in real time
- **Send payment requests** — opens native SMS on your phone pre-filled with "You owe [Name] $X.XX" for every non-payer

### Technical Highlights
- **Claude Vision API** for accurate receipt OCR and structured data extraction
- **Surgical DOM updates** — only the changed row re-renders on assignment, zero flicker
- **localStorage** for cross-session contact memory
- **Camera API** with rear-camera preference and gallery upload fallback
- Zero dependencies — pure HTML, CSS, vanilla JavaScript
- Single `index.html` file — deploy anywhere static hosting works

---

## 🚀 Live Demo

**[https://your-username.github.io/splitway/](https://your-username.github.io/splitway/)**

> Update this link after deploying to GitHub Pages

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

## 💻 Local Development

The app is a single static file. Run any local server — camera requires HTTPS or `localhost`.

```bash
# Python
python -m http.server 8000

# Node
npx http-server -p 8000

# Then open http://localhost:8000
```

> **Note:** The Claude Vision receipt scanning requires network access to `api.anthropic.com`. This works automatically on GitHub Pages (HTTPS). Locally, the app falls back gracefully if the API is unreachable.

---

## 🚢 Deploy to GitHub Pages

```bash
# 1. Create a new repo on github.com named "splitway"

# 2. Push the files
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR-USERNAME/splitway.git
git branch -M main
git push -u origin main

# 3. Enable GitHub Pages
# Repo Settings → Pages → Source: main / root → Save
# Live at: https://YOUR-USERNAME.github.io/splitway/
```

Full step-by-step instructions in [DEPLOYMENT.md](DEPLOYMENT.md).

---

## 🔮 Potential Future Enhancements

- [ ] Real payment integration (Venmo, Zelle, Cash App deep links)
- [ ] Save and reload past splits
- [ ] Dark mode
- [ ] Progressive Web App (PWA) / installable
- [ ] Multiple currencies
- [ ] Export split to PDF or share link

---

## 📝 License

MIT — see [LICENSE](LICENSE)

---

## 👤 Author

**Your Name**
- GitHub: [@your-username](https://github.com/ohndira)
- LinkedIn: [your-profile](www.linkedin.com/in/johndiradoorian)

---

> Built as a portfolio project demonstrating AI-native product thinking, mobile web development, and real-world UX design for the commerce/payments space.
