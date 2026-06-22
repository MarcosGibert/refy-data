# Refy Data

<p align="center">
  <img src="icono.png" alt="Refy Data icon" width="96">
</p>

Refy Data is a companion dashboard for Refy Journal. It imports journal JSON exports and turns daily entries, mood ratings, activities, and emotions into yearly visual summaries.

## Features

- Imports JSON exports from Refy Journal.
- Supports both legacy array exports and the newer export format with editable activity/emotion lists.
- Migrates old combined tags such as `School/work` and `Confused/thoughtful` into separate tags.
- Derives activity and emotion labels dynamically from the imported entries.
- Preserves historical tags in yearly analysis, even if those tags are no longer active in the journal app.
- Shows yearly summary metrics for entries, average mood, variance, and best month.
- Displays monthly tables and charts for:
  - Average mood
  - Mood variance
  - Mood range
  - Emotion share
  - Activity share
  - Emotion density
  - Activity density

## Tech Stack

- HTML
- CSS
- JavaScript
- [Chart.js](https://www.chartjs.org/) for charts

## Running Locally

Open `index.html` in a browser, or serve the folder locally:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

Because the dashboard loads Chart.js from a CDN, an internet connection is required for charts to render.

## Data Model

The dashboard accepts:

- Legacy Refy exports as a plain array of entries.
- New Refy Journal exports with `entries`, `activities`, and `emotions`.

For analysis, activity and emotion labels are computed from the entries in the selected year. This makes historical analysis resilient to tag changes over time.

## Project Context

This project was built to make Refy Journal data easier to explore at a higher level. While the journal app focuses on daily reflection, this dashboard focuses on longer-term patterns across months and years.

