# Dancetime v2026 - dance ranking analytics 2026

> **A browser-based ballroom dance ranking and heat analysis tool that transforms NDCA competition results into ELO ratings, leaderboards, and competitor insights for the 2026 release.**

[![Platform](https://img.shields.io/badge/Platform-web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/henryhallvdu1420/dancetime-ballroom-elo?style=flat-square)](https://github.com/henryhallvdu1420/dancetime-ballroom-elo)

---

<p align="center">
  <a href="https://henryhallvdu1420.github.io/dancetime-ballroom-elo/">
    <img src="https://img.shields.io/badge/Download-Dancetime%20Latest-brightgreen?style=for-the-badge" alt="Download Dancetime">
  </a>
</p>

> **[Download Dancetime v2026](https://henryhallvdu1420.github.io/dancetime-ballroom-elo/)**

---

[Download Latest Build](https://henryhallvdu1420.github.io/dancetime-ballroom-elo/)

---

## Overview

Dancetime is a web application for examining competitive ballroom dance results. It retrieves event information through the NDCA API and turns raw competition data into accessible ranking and analysis views. Dancers, coaches, event organizers, and followers of the sport can use it to study results and performance patterns across competitions.

The project brings heat-level exploration and rating analysis together. ELO calculations, leaderboard views, and competitor-focused statistics make it easier to compare head-to-head results, identify shared heats, and follow changes over time.

---

## What It Provides

- Imports competition results from the NDCA API
- Produces ELO ratings over multiple competitions
- Offers an interactive heat browser built around heat cards
- Marks contested couples with dedicated badges
- Displays competitor schedules and head-to-head performance
- Organizes the leaderboard around shared-heat clusters
- Provides win percentages as additional ranking context
- Includes a scrape, process, and publish pipeline workflow

---

## Getting Started

Clone the repository, then move into the project directory:

```bash
git clone https://github.com/henryhallvdu1420/dancetime-ballroom-elo.git
cd dancetime
```

When using the pipeline utilities, execute the appropriate CLI stage from the project environment. This retrieves the source data, transforms it, and publishes the generated results before the site is opened.

The single-page application can then be served through a local web server or deployed with a static hosting configuration of your choice.

---

## Workflow

The normal data path consists of these steps:

1. Retrieve competition results from the NDCA API.
2. Process the results to calculate ratings and establish heat relationships.
3. Publish the generated dataset for the web application.
4. Browse leaderboards, competitor information, and heat analysis in the interface.

The pipeline commands can be run in sequence:

```bash
scrape
process
publish
```

After publishing completes, the heat browser can be used to examine specific heats. Competitor pages provide scheduling and statistical details, while the leaderboard supports comparisons across events with shared participation.

---

## Configuration

The application and pipeline deployment determine how configuration is handled. For a custom data workflow, place API access details, processing locations, and publication destinations in the project environment or build configuration.

A representative configuration shape is:

```json
{
  "api": "NDCA",
  "mode": "pipeline",
  "output": "published-data"
}
```

---

## Requirements

- A web browser for running the single-page application
- Access to NDCA competition data
- A local or hosted environment that can serve static web content
- A workflow environment able to execute the scrape, process, and publish stages
- HTML-compatible hosting for the front-end build

---

## Frequently Asked Questions

**How can I refresh the rankings and results?**  
Run the pipeline again. It will retrieve updated results, calculate the ratings again, and publish the refreshed data.

**Where are configuration changes made?**  
Modify the application or pipeline configuration used by your local or hosted deployment. Its precise location varies with the deployment method.

**Why might the leaderboard be missing information?**  
Confirm that the most recent NDCA data was successfully fetched and processed before the publish step was run.

**Is Dancetime deployable as an independent website?**  
Yes. Dancetime is designed as a web-based single-page application and can be served as a static site after the data pipeline has completed.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
