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

## 📂 My Other Open-Source Projects

-   **[AI-Trader-For-MT4](https://github.com/toki-plus/ai-trader-for-mt4)**: A revolutionary open-source framework that transforms a Large Language Model (LLM) into an autonomous trading agent for the MetaTrader 4 (MT4) platform.
-   **[AI Mixed Cut](https://github.com/toki-plus/ai-mixed-cut)**: A groundbreaking AI content re-creation engine that deconstructs viral videos into a creative library and automatically generates new, original videos using a "Deconstruct-Reconstruct" model.
-   **[AI Video Workflow](https://github.com/toki-plus/ai-video-workflow)**: A fully automated AI-native video generation pipeline, integrating Text-to-Image, Image-to-Video, and Text-to-Music models to create AIGC short videos with one click.
-   **[AI Highlight Clip](https://github.com/toki-plus/ai-highlight-clip)**: An AI-driven intelligent clipping tool that automatically analyzes and extracts "highlight moments" from long-form videos and generates viral titles.
-   **[AI TTV Workflow](https://github.com/toki-plus/ai-ttv-workflow)**: An AI-powered Text-to-Video tool that automatically converts any script into a short video with voiceover, subtitles, and a cover, supporting script extraction/re-creation/translation.
-   **[AB Video Deduplicator](https://github.com/toki-plus/AB-Video-Deduplicator)**: Utilizes an innovative "High-Framerate Frame-Mixing" technique to fundamentally alter a video's data fingerprint, designed to bypass originality detection/deduplication mechanisms on major short-video platforms.
-   **[Video Mover](https://github.com/toki-plus/video-mover)**: A fully automated content creation pipeline that monitors and downloads videos, performs multi-dimensional deduplication, generates AI titles, and publishes to multiple platforms with one click.

## 🤝 Contributing

Contributions of any kind are welcome! If you have ideas for new features, found a bug, or have any suggestions for improvement, please:
-   Submit an [Issue](https://github.com/toki-plus/auto-usps-tracker/issues) to start a discussion.
-   Fork this repository and submit a [Pull Request](https://github.com/toki-plus/auto-usps-tracker/pulls).

If this project has been helpful to you, please consider giving it a ⭐!

## 📜 License

This project is open-sourced under the MIT License. See the [LICENSE](LICENSE) file for details.
