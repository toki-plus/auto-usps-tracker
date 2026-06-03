# Auto USPS Tracker

[简体中文](./README.md) | [English](./README_en.md)

[![GitHub stars](https://img.shields.io/github/stars/toki-plus/auto-usps-tracker?style=social)](https://github.com/toki-plus/auto-usps-tracker/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/toki-plus/auto-usps-tracker?style=social)](https://github.com/toki-plus/auto-usps-tracker/network/members)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/toki-plus/auto-usps-tracker/pulls)

**`Auto USPS Tracker` is a desktop application designed for cross-border e-commerce sellers and users who need to track a large number of USPS packages. It fully automates the process of bulk-scraping tracking information from the official USPS website and generates beautifully formatted Excel reports.**

Are you still struggling with manually checking the tracking status of hundreds or thousands of USPS orders? This project aims to simplify this tedious and time-consuming workflow into a one-click operation, significantly boosting your productivity.

<p align="center">
  <a href="https://www.bilibili.com/" target="_blank">
    <img src="" alt="Click to watch the demo video on Bilibili (Coming Soon)" width="800"/>
  </a>
  <br>
  <em>(Click the cover to watch the HD demo video on Bilibili)</em>
</p>

---

## ✨ Core Features

-   **📦 High-Volume Concurrent Tracking**: Supports inputting thousands of tracking numbers at once. The program automatically processes them in batches and multiple processes to maximize network and CPU resource utilization.
-   **🛡️ Intelligent Anti-Blocking Scraping**:
    -   Based on the modern **Playwright** framework to simulate a real browser environment.
    -   Built-in advanced "Stealth" anti-blocking techniques to effectively bypass bot detection from services like Cloudflare, ensuring stable and successful queries.
-   **📋 Comprehensive Information Extraction**:
    -   Fetches not only the **latest status** of the package (e.g., "Delivered", "In Transit") but also the **detailed status description** and the **complete tracking history**.
    -   Automatically handles failed queries or invalid tracking numbers, clearly marking them in the report.
-   **📊 Formatted Excel Report Export**:
    -   Automatically organizes all query results and exports them into a `.xlsx` Excel file.
    -   The report is professionally formatted with **colored headers, auto-wrapped text, borders**, and **self-adjusting column widths** for clarity and readability.
-   **🌐 Proxy Support & Simple GUI**:
    -   Supports configuration of HTTP proxy servers to handle complex network environments.
    -   Provides a clean and intuitive Graphical User Interface (GUI), making all operations straightforward without requiring any programming knowledge.

## 📸 Screenshots

<p align="center">
  <img src="./images/cover_software01.png" alt="Main UI" width="800"/>
  <br>
  <em>The main user interface: Simple design, powerful functionality.</em>
</p>
<p align="center">
  <img src="./images/cover_software02.png" alt="Exported Spreadsheet" width="800"/>
  <br>
  <em>Exported Spreadsheet: Clear and polished style.</em>
</p>

## 🚀 Quick Start

### System Requirements

-   **OS**: Windows 10 or later.
-   **Browser**: Google Chrome installed.

### Installation & Launch

-   **Download Link**: https://download.llxoxll.com/latest/yanqu_usps_tracker

---

<p align="center">
  <strong>For custom development or technical inquiries, please connect via:</strong>
</p>
<table align="center">
  <tr>
    <td align="center">
      <img src="./images/wechat.png" alt="WeChat QR Code" width="200"/>
      <br />
      <sub><b>WeChat</b></sub>
      <br />
      <sub>WeChat ID: toki-plus</sub>
      <br />
      <sub>(Please include your purpose when adding me)</sub>
    </td>
    <td align="center">
      <img src="./images/gzh.png" alt="Public Account QR Code" width="200"/>
      <br />
      <sub><b>Public Account</b></sub>
      <br />
      <sub>Scan for tech articles</sub>
    </td>
  </tr>
</table>

## 📂 My Other Open-Source Projects

-   **[AI-Trader-For-MT5](https://github.com/toki-plus/ai-trader-for-mt5)**: An AI trading assistant and EA engineering framework for MetaTrader 5, combining MQL5, Python, MCP-style tool services, risk modules, and private custom development.
-   **[Netease Downloader](https://github.com/toki-plus/netease-downloader)**: An elegant, feature-rich desktop application for downloading high-quality and lossless music from Netease Cloud Music, with support for playlists, albums, QR login, and automatic metadata tagging.
-   **[AI-Trader-For-MT4](https://github.com/toki-plus/ai-trader-for-mt4)**: An LLM-driven autonomous MT4 trading robot framework that turns large language models into AI trading agents capable of sensing, reasoning, and acting on MetaTrader 4.
-   **[AI Mixed Cut](https://github.com/toki-plus/ai-mixed-cut)**: An AI content re-creation and mixed-cut tool that deconstructs existing videos into creative assets and automatically generates new short-form videos.
-   **[AI Video Workflow](https://github.com/toki-plus/ai-video-workflow)**: A fully automated AI-native video generation workflow integrating text-to-image, image-to-video, and text-to-music models for one-click AIGC short video creation.
-   **[AI Highlight Clip](https://github.com/toki-plus/ai-highlight-clip)**: An AI-powered intelligent clipping tool that automatically analyzes long videos and extracts highlight clips for short-form content distribution.
-   **[AI TTV Workflow](https://github.com/toki-plus/ai-ttv-workflow)**: An AI-powered text-to-video workflow that turns scripts into short videos with voiceover, subtitles, and cover images.
-   **[AB Video Deduplicator](https://github.com/toki-plus/AB-Video-Deduplicator)**: A video deduplication and fingerprint-reconstruction tool that changes video data characteristics through high-frame-rate frame sampling and blending.
-   **[Video Mover](https://github.com/toki-plus/video-mover)**: An automated content creation pipeline for video monitoring, downloading, multi-dimensional processing, AI title generation, and multi-platform publishing.


## 🤝 Contributing

Contributions of any kind are welcome! If you have ideas for new features, found a bug, or have any suggestions for improvement, please:
-   Submit an [Issue](https://github.com/toki-plus/auto-usps-tracker/issues) to start a discussion.
-   Fork this repository and submit a [Pull Request](https://github.com/toki-plus/auto-usps-tracker/pulls).

If this project has been helpful to you, please consider giving it a ⭐!

## 📜 License

This project is open-sourced under the MIT License. See the [LICENSE](LICENSE) file for details.





