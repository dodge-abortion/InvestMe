# ⚡ VentureAI

**AI-powered platform that instantly generates investor-grade business plans and connects startups with capital.**

VentureAI bridges the gap between raw startup ideas and venture-ready pitches. Describe your idea, and AI generates a full business plan scored against global VC standards — then list it on a marketplace where investors can discover, evaluate, and fund it.

---

## 🎯 Problem

Founders spend weeks (or hire expensive consultants) to turn an idea into a structured business plan that investors actually take seriously. Meanwhile, investors sift through hundreds of unstructured, inconsistent pitch decks with no standardized way to compare opportunities.

## 💡 Solution

VentureAI uses Claude AI to:
1. Take a raw idea (with capital, geography, and target market as inputs)
2. Generate a complete business plan using established frameworks
3. Score the idea against global investment-readiness standards
4. Publish it to a marketplace where investors can browse, evaluate, and invest

---

## ✨ Features

### For Founders
- AI-generated business plan from a short idea description
- Automatic scoring across 6 dimensions: market potential, team viability, financial model, innovation, scalability, competitive advantage
- Industry-standard frameworks applied automatically:
  - **Lean Canvas**
  - **TAM / SAM / SOM** market sizing
  - **SWOT analysis**
  - **Porter's Five Forces**
  - Financial projections (revenue, burn rate, runway, break-even)
- Investment-readiness grade (A+ to C) with identified gaps
- One-click publish to the investor marketplace

### For Investors
- Browse a marketplace of AI-scored startup opportunities
- Filter by industry, country, funding stage
- See key metrics at a glance: TAM, growth rate, margin, equity offered, capital raised vs. target
- Initiate investment directly from a startup's card

### Role-based experience
- Single sign-up flow splits into two distinct dashboards: **Founder** or **Investor**

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React |
| AI Engine | Claude API (Anthropic) — Sonnet model |
| Database & Auth | Supabase |
| Hosting | Vercel |
| Payments (planned) | Stripe |
| Identity Verification (planned) | KYC provider (e.g. Sumsub) |

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- An [Anthropic API key](https://console.anthropic.com)
- A [Supabase](https://supabase.com) project (free tier)

### Installation

```bash
git clone https://github.com/your-username/ventureai.git
cd ventureai
npm install
```

### Environment Variables

Create a `.env` file:

```
ANTHROPIC_API_KEY=your_key_here
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_anon_key
```

### Run locally

```bash
npm run dev
```

---

## 📐 How It Works

1. **Founder submits an idea** — description, industry, target country, target market, available capital, and current stage.
2. **Claude generates a structured plan** — a single prompt returns a JSON object containing the full business plan, framework breakdowns, scores, and financial projections.
3. **The idea is scored and graded** — an overall investment grade (A+–C) is calculated from sub-scores across six dimensions.
4. **Founder publishes to the marketplace** — the structured plan becomes a browsable card for investors.
5. **Investors discover and invest** — filter by sector/geo/stage, review AI-generated metrics, and submit an investment request.

---

## 🗺️ Roadmap

- [ ] User authentication (founder / investor roles)
- [ ] Persistent startup & investment database (Supabase)
- [ ] Real investor verification (KYC)
- [ ] In-app messaging between founders and investors
- [ ] Stripe-based escrow for investment transactions
- [ ] Public idea board for unclaimed/unrealized ideas
- [ ] Multi-language support
- [ ] Mobile app

---

## ⚠️ Status

This is an early-stage prototype. Core AI generation and UI flows are functional; authentication, persistence, and payments are not yet implemented. Not production-ready — do not use for real financial transactions yet.

---

## 📄 License

MIT

---

## 🤝 Contributing

This project is in early development. Issues and pull requests are welcome — especially around the data model, investor verification flow, and financial projection accuracy.
