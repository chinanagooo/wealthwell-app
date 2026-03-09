# WealthWell — Wealth Wellness Hub

> Your complete financial command centre. Track every asset, measure your wellness, and simulate your future. Built for Singapore. Built by Singaporeans.

## Preview

| Dashboard | Portfolio | Expenses |
|-----------|-----------|----------|
| Wealth Wellness Score, net worth overview, and key metrics | Full balance sheet with assets and liabilities | Daily spending tracker with category breakdown |

---

## Features of WealthWell Application

- **Onboarding Wizard** — 6-step profile setup before accessing the app
- **Unified Portfolio** — Track assets across cash, stocks, crypto, property, CPF, and more
- **Wellness Score** — Dynamically computed across 6 financial health dimensions
- **Scenario Lab** — Simulate market crashes, job loss, rate hikes, and retirement
- **Action Centre** — AI-generated priority actions based on your real data
- **Expense Tracker** — Daily spending log with category breakdown and limit alerts
- **localStorage Persistence** — All data is saved locally in your browser
- **Profile Reset** — Start fresh anytime from the sidebar
- **SGD-first** — Multi-currency support with SGD as default
- **Pro Mode** — Bloomberg-style advanced analytics panel

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 18 + Vite 5 |
| Charts | Recharts |
| Styling | Inline styles + CSS custom properties |
| Font | Sora (Google Fonts) |
| Storage | Browser localStorage |
| Container | Docker + nginx |

---

## Initialise Application

### Option A — Docker (Recommended)

```bash
# 1. Clone the repo
git clone https://github.com/chinanagooo/wealthwell-app.git
cd wealthwell-app

# 2. Build the Docker image
docker build -t wealthwell-app .

# 3. Run the container
docker run -p 8080:80 -d wealthwell-app

# 4. Open in browser
# http://localhost:8080
```

### Option B — Local Development

```bash
# 1. Clone the repo
git clone https://github.com/chinanagooo/wealthwell-app.git
cd wealthwell-app

# 2. Install dependencies
npm install

# 3. Start dev server
npm run dev

# 4. Open in browser
# http://localhost:5173
```

---

## Project Structure Layout

```
wealthwell-app/
├── public/                 # Static assets
├── src/
│   ├── App.jsx             # Main application (onboarding + all screens)
│   ├── main.jsx            # Vite entry point
│   └── index.css           # Global reset and base styles
├── index.html              # HTML entry with font preload
├── package.json            # Dependencies
├── vite.config.js          # Vite configuration
├── Dockerfile              # Multi-stage Docker build
└── README.md
```

---

## Docker Commands Reference

```bash
# Build image
docker build -t wealthwell-app .

# Run container (port 8080)
docker run -p 8080:80 -d wealthwell-app

# View running containers
docker ps

# Stop container
docker stop <container_id>

# Remove container
docker rm <container_id>

# Remove image (before rebuilding)
docker rmi wealthwell-app

# Rebuild after pulling changes
git pull origin main
docker build -t wealthwell-app .
docker run -p 8080:80 -d wealthwell-app
```

---

## Available Scripts

```bash
npm run dev       # Start development server (localhost:5173)
npm run build     # Build for production → /dist
npm run preview   # Preview production build locally
npm run lint      # Run ESLint
```

---

## Application Screens

| Screen | Description |
|--------|-------------|
| **Home** | Net worth hero, wellness score, portfolio donut chart, top metrics |
| **Portfolio** | Full balance sheet — add, edit, and delete assets and liabilities |
| **Insights** | 6 wellness dimension scores + Pro Bloomberg analytics panel |
| **Scenario Lab** | Interactive sliders to simulate financial shocks and events |
| **Action Centre** | Prioritised flash cards with recommended financial actions |
| **Expenses** | Daily spending tracker with limit alerts and category breakdown |
| **Trust Centre** | Connected accounts, security info, and data reset |

---

## Privacy concerns

All data is stored **locally in your browser** using `localStorage`. No data is sent to any server. You can clear everything at any time using the **New Profile / Reset** button in the sidebar.

---

## Contributing to the repository

1. Fork the repository
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Commit your changes: `git commit -m "feat: add your feature"`
4. Push to the branch: `git push origin feat/your-feature`
5. Open a Pull Request

---

## License

[chinanagooo](https://github.com/chinanagooo)

---

<div align="center">
  <strong>Pursue your financial freedom.</strong>
</div>
