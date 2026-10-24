# ProteoPipe
> *by Mk tech*

[![License: MIT](https://img.shields.io/badge/License-MIT-peach.svg?style=flat-square&color=FFB085&labelColor=050507)](LICENSE)
[![Platform: Web / GitHub Pages](https://img.shields.io/badge/Platform-Client--Side_SPA-peach.svg?style=flat-square&color=FFB085&labelColor=050507)](https://github.com)
[![Status: Production](https://img.shields.io/badge/Status-Active-peach.svg?style=flat-square&color=FFB085&labelColor=050507)]()

**ProteoPipe** is a high-performance, client-side bioinformatics pipeline and biomarker discovery platform. Designed to overcome the payload ceilings and timeouts of traditional serverless infrastructure, ProteoPipe decompresses and analyzes multi-omics datasets (up to 300 MB) directly within browser memory. 

The engine harmonizes heterogeneous mass spectrometry matrices, queries public biological APIs in real time, generates 3D molecular structures from AlphaFold DB, and compiles comprehensive, 12-sheet audit workbooks matching clinical proteomics standards.

---

## Key Capabilities

- **Zero-Serverless Client Architecture**: Bypasses server payload limits (such as Vercel's 4.5 MB ceiling) by executing archive decompression, tabular parsing, and workbook generation entirely in client-side RAM using Web Workers and `JSZip`.
- **Strict Ingestion Guardrails**: Drag-and-drop ingestion accepting `.zip` archives with real-time validation enforcing a strict 300 MB limit.
- **5-Stage Execution Stream**: Live visual percentage tracking paired with an embedded terminal log streaming data ingestion, matrix parsing, API harmonization, scoring, and assembly.
- **Dynamic Biological Enrichment**: Automated live querying against the **UniProtKB REST API** for accession mapping and functional summaries, and **AlphaFold DB / RCSB PDB** for predicted 3D structures.
- **Interactive Visualizations**:
  - **Volcano Plot**: Dynamic scatter plotting of Log2 Fold Change against $-\log_{10}(\text{FDR})$ with custom significance thresholds.
  - **Biomarker Ranking Waterfall**: Multi-parameter evidence subtotal scoring ranking top candidates across studies.
  - **3D Molecular Structure Studio**: Powered by `3Dmol.js`, rendering ribbon and cartoon representations of candidates in real time.
- **12-Sheet Master Excel Export**: One-click synthesis of the complete analysis into a single, multi-tabbed spreadsheet (`CRC_Biomarker_Analysis_Master.xlsx`) using `ExcelJS`.

---

## Visual Design & Aesthetics

ProteoPipe pairs high-density data visualization with an obsidian-bioluminescent design language:

| Design Token | Specification | Preview / Usage |
| :--- | :--- | :--- |
| **Canvas Background** | `#050507` (Deep Obsidian) | Full screen base |
| **Surface Containers** | `#0E1017` / `#111319` | Glassmorphic cards with glowing borders |
| **Primary Accent** | `#FFB085` / `#FF9776` (Peach) | Active states, interactive tabs, progress fills |
| **Peach Glow** | `0 0 18px rgba(255, 176, 133, 0.45)` | Title treatments and focal highlights |
| **Primary Typography** | `Californian FB`, `Playfair Display`, serif | Headers, metrics, and report titles |
| **Monospace / Terminal** | `JetBrains Mono`, `Fira Code`, monospace | Pipeline status logs and raw accessions |

---

## 12-Sheet Data Schema Architecture

The generated export strictly adheres to the multi-dataset biomarker discovery schema:
