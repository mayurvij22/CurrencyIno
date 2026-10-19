<div align="center">

# 💱 Currency Converter

**Convert between 150+ world currencies with live exchange rates and country flags.**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Vercel](https://img.shields.io/badge/deployed%20on-Vercel-000000?logo=vercel&logoColor=white)

### [🌐 Live demo](https://currency-ino.vercel.app)

</div>

---

## ✨ Features

- Convert any amount between currencies chosen from two dropdowns (defaults: **USD → INR**)
- **Live exchange rates** fetched from the free [fawazahmed0 Currency API](https://github.com/fawazahmed0/exchange-api)
- The **country flag** updates automatically when you change a currency ([FlagsAPI](https://flagsapi.com))
- Input validation: empty or invalid amounts fall back to `1`
- Rates are fetched on page load and on every conversion

## 🛠️ Tech stack

| Layer | Technology |
|---|---|
| UI | HTML5, CSS3 |
| Logic | Vanilla JavaScript (`fetch`, async/await) |
| Data | Currency API (rates) · FlagsAPI (flag images) |
| Hosting | Vercel |

## 🚀 Run locally

```bash
git clone https://github.com/mayurvij22/CurrencyIno.git
cd CurrencyIno
# open index.html in your browser (internet connection needed for live rates)
```

## 📁 Project structure

```text
├── index.html   # Converter form (amount, from/to dropdowns, result)
├── style.css    # Styling
├── codes.js     # Currency code → country code map (used for the dropdowns and flags)
└── index.js     # Populates the dropdowns, fetches rates, updates flags
```

## 🧠 How it works

1. `codes.js` maps each currency code to a country code, for example `INR → IN`.
2. Both dropdowns are filled from that map, and changing one swaps in the matching flag.
3. On **Get Exchange Rate**, the app requests `/{from}/{to}.json` from the Currency API and multiplies the amount by the returned rate.

---

<div align="center">

Made by **[Mayur Patil](https://github.com/mayurvij22)**

</div>
