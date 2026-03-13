# DBSCAN vs KMeans — Clustering Showdown 🥊

An interactive, browser-based comparison of two fundamental clustering algorithms. Built for **conference talks, workshops, and educational demos**.

**🔗 [Live Demo →](https://michalbojkogdansk.github.io/clustering-showdown/)**

![Screenshot](https://img.shields.io/badge/algorithms-2-indigo) ![Screenshot](https://img.shields.io/badge/datasets-3-pink) ![Screenshot](https://img.shields.io/badge/dependencies-0-green) ![Screenshot](https://img.shields.io/badge/build_step-none-brightgreen)

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| **3 Datasets** | Server Logs (spherical + anomalies), Sales Data (4 customer segments), Geo Clusters (non-convex crescents) |
| **Side-by-side visualization** | KMeans (indigo) vs DBSCAN (pink) rendered on HTML5 Canvas |
| **Live parameter controls** | Adjust `k`, `ε` (epsilon), and `minPoints` with sliders — with hover tooltips explaining each |
| **Manual execution** | Click **Run Analysis** to execute — no auto-running, so you control the pace during demos |
| **Benchmark panel** | Execution time, cluster count, noise detection, silhouette score with winner badges |
| **Data preview** | Scrollable table showing the raw data points for each dataset |
| **Algorithm code (JS)** | The actual JavaScript KMeans & DBSCAN implementations used in the demo |
| **Python code samples** | Production-ready sklearn snippets for KMeans, DBSCAN, and a full comparison benchmark |
| **Dark / Light mode** | Toggle with 🌙/☀️ button — respects system preference, persists in localStorage |
| **Zero dependencies** | Single HTML file, no build step, no server — just open in a browser |

## 🚀 Quick Start

### Option 1: GitHub Pages (already deployed)
Visit **[michalbojkogdansk.github.io/clustering-showdown](https://michalbojkogdansk.github.io/clustering-showdown/)**

### Option 2: Local
```bash
git clone https://github.com/michalbojkogdansk/clustering-showdown.git
cd clustering-showdown
open index.html  # or just double-click it
```

### Option 3: Any static host
Upload `index.html` to Netlify, Vercel, S3, or any static file server. Done.

## 📊 Datasets

### 🖥️ Server Logs
- **X-axis:** CPU Usage (%) | **Y-axis:** Memory Usage (%)
- 3 spherical clusters (normal traffic, high load, memory leak) + 15 scattered anomalies
- **Best for demonstrating:** Anomaly detection — DBSCAN identifies outliers as noise, KMeans forces them into clusters

### 🛒 Sales Data
- **X-axis:** Average Order Value ($) | **Y-axis:** Purchase Frequency (orders/year)
- 4 customer segments (bargain hunters, casual buyers, whales, VIPs) + 12 noise points
- **Best for demonstrating:** Customer segmentation — when you know k vs. when you want to discover it

### 🌍 Geo Clusters
- **X-axis:** Longitude | **Y-axis:** Latitude
- Non-convex crescent-moon shape + dense blob + 18 noise points
- **Best for demonstrating:** KMeans' failure mode — it cannot capture non-convex shapes. DBSCAN handles them naturally.

## 🎓 Parameter Guide

| Parameter | Algorithm | What it does | Tips |
|-----------|-----------|-------------|------|
| **k** | KMeans | Number of clusters to create | Use Elbow Method or Silhouette Score to find optimal value |
| **ε (epsilon)** | DBSCAN | Maximum neighborhood radius | Depends on data scale — always normalize first. Start with k-distance plot |
| **minPoints** | DBSCAN | Minimum neighbors to form a core point | Rule of thumb: `2 × dimensions`. For 2D data, try 4–5 |

## 🧠 When to Use Which?

| Scenario | Recommended | Why |
|----------|-------------|-----|
| You know how many groups exist | **KMeans** | You can specify k directly |
| Data has noise/outliers | **DBSCAN** | Automatically identifies noise points |
| Clusters are spherical/convex | **KMeans** | Optimized for this exact shape |
| Clusters are non-convex (crescents, rings) | **DBSCAN** | Follows density, not distance to centroids |
| Need consistent, fast results | **KMeans** | O(nkt) vs DBSCAN's O(n²) naive implementation |
| Feature scales vary wildly | **DBSCAN** | After normalization — ε is distance-based |
| Streaming/real-time data | **KMeans** | Easy to assign new points to existing centroids |

## 🏗️ Technical Details

- **Algorithms:** Pure JavaScript implementations — no ML libraries
- **KMeans:** Uses KMeans++ initialization for better convergence
- **DBSCAN:** Naive O(n²) implementation (fine for demo-sized datasets)
- **Silhouette Score:** Sampled approximation (up to 200 points) for performance
- **RNG:** Deterministic (mulberry32 seeded at 42) — same data every time
- **Rendering:** HTML5 Canvas with DPR-aware scaling
- **Styling:** Tailwind CSS + DaisyUI via CDN

## 📄 License

MIT — use it freely for your talks, courses, and workshops.

---

*Built with ❤️ for the data science community.*
