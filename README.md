# 📐 Data Engineering Foundations

Interactive visual lectures for data engineering concepts. Zero build step — just static HTML served via GitHub Pages.

**🔗 [Live Site →](https://michalbojkogdansk.github.io/clustering-showdown/)**

---

## Topics

| Topic | Status | Description |
|-------|--------|-------------|
| 🔮 [Clustering](https://michalbojkogdansk.github.io/clustering-showdown/clustering.html) | ✅ Live | KMeans vs DBSCAN — interactive comparison with benchmarks and business analysis |
| 📊 Bins & Histograms | 🚧 Coming Soon | Data distribution, binning strategies, detecting skewness |
| 🔥 Failure Detection | 🚧 Coming Soon | From threshold alerts to ML-powered anomaly detection |
| 📈 Regression | 🚧 Coming Soon | Linear to polynomial regression with business interpretation |
| ⚡ Spikes & Anomalies | 🚧 Coming Soon | Statistical methods for detecting unusual patterns in metrics |
| 📋 Log-Driven Dev | 🚧 Coming Soon | Structured logging as a foundation for observability |

## Features

- **🌗 Dark / Light mode** — persists across all pages via localStorage
- **📊 Interactive visualizations** — all charts rendered client-side on canvas
- **💼 Business-oriented analysis** — benchmark results explained in plain business language
- **🔴 Anomaly highlighting** — DBSCAN noise points shown in red with glow effect
- **📈 Scaling benchmarks** — test S → XXXL dataset sizes to see O(n²) vs O(n·k) in practice
- **📝 Collapsible code** — algorithm source code (JS + Python) available on demand
- **🏗️ Zero build step** — vanilla HTML/CSS/JS, deployable anywhere

## Architecture

```
├── index.html              # Landing page — topic grid
├── clustering.html         # KMeans vs DBSCAN showdown
├── bins.html               # Placeholder
├── failure-detection.html  # Placeholder
├── regression.html         # Placeholder
├── spikes.html             # Placeholder
├── log-driven.html         # Placeholder
├── shared/
│   ├── style.css           # Shared styles (Azure dashboard aesthetic)
│   └── nav.js              # Navigation bar (self-injecting)
└── README.md
```

## Tech Stack

- **HTML5 Canvas** for all visualizations
- **Tailwind CSS** + **DaisyUI** via CDN
- **PrismJS** for syntax highlighting
- **GitHub Pages** for hosting
- **100% client-side** — all computation runs in the browser

## Running Locally

Just open `index.html` in a browser. No server, no npm, no build.

```bash
# Or use any static server:
python3 -m http.server 8000
```

## License

MIT
