# 📊 Dashboard Application

A high-performance, real-time developer dashboard application built with **SvelteKit (Svelte 5)**. Designed for lightning-fast responsiveness, real-time data visualisations, and clean system monitoring interfaces.

## 🚀 Live Demo

The application is deployed and fully operational at:  
👉 **[https://activity-dashboard-production.up.railway.app/calendar](https://activity-dashboard-production.up.railway.app/calendar)**

---

## ✨ Features

- **Real-Time Logs Viewer (`/logs`)**: Stream, search, filter, and inspect application or system logs dynamically with zero latency.
- **Svelte 5 Runes**: Built using the latest Svelte reactivity model for highly optimal client-side performance and state tracking.
- **SSR & Client-side Fallbacks**: Hybrid rendering strategy utilizing SvelteKit's client router with robust Node.js server fallback support.
- **Responsive Design**: Tailored to look clean and legible on any device, from mobile layouts to ultra-wide monitor screens.

---

## ⚙️ Core Architecture (MarkdownDB Integration)

Unlike traditional databases, this application treats **Markdown files as a queryable database** using **MarkdownDB (`mddb`)**:

- **Metadata Extraction**: Recursively scans log/document directories via `readdirp` to extract rich YAML frontmatter, markdown tags, levels, dates, and cross-document links.
- **SQLite Indexing**: Compiles this structured file-based metadata into a lightweight, local SQLite database (`markdown.db`) for high-performance server-side retrieval.
- **Fast API Queries**: Leverages the MarkdownDB Node.js API directly in SvelteKit server-side functions to filter, sort, and search logs instantly.

---

## 🛠️ Tech Stack

- **Frontend & Meta-Framework**: SvelteKit (Svelte 5)
- **Markdown Database Engine**: MarkdownDB (`mddb` via `readdirp`)
- **Database Cache**: SQLite
- **Server Environment**: Node.js (`adapter-node` production build)
- **Hosting & Deployment**: Railway

---

## 💻 Getting Started

Follow these steps to set up the dashboard locally:

### 1. Clone the repository
```bash
git clone <your-repository-url>
cd dashboard
```

### 2. Install dependencies
```bash
npm install
```

### 3. Run the development server
```bash
npm run dev -- --open
```

### 4. Build for production
```bash
npm run build
npm run preview
```
