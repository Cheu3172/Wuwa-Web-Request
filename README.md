# Wuwa-Web-Request
A repository for archiving the Web Request/JSON data responses from the official *Wuthering Waves* launcher and game client APIs.

Maintained by [Acheuy](https://github.com/Cheu3172).
## Repository Structure
This repository is organized by game/launcher version. Each version has its own dedicated folder containing the JSON data relevant to that specific release.

```
.
├── api.json
├── 2.6.0v/
│   ├── globalClient.json
│   ├── news.json
│   ├── socials.json
│   └── wallpaper.json
├── 0.0.0v/
│   └── ... (newer version's files)
└── README.md
```
## Files
### 1\. `api.json` (Root Directory)
This contains the API endpoint URLs used by the official launcher. This file will be kept as up-to-date as possible to ensure the links are always current.

**Structure:**
```json
{
  "news": {
    "url": "https://prod-alicdn-gamestarter.kurogame.com/...",
    "description": "Retrieves news, notices, and events."
  },
  "wallpapers": {
    "url": "https://prod-alicdn-gamestarter.kurogame.com/...",
    "description": "Fetches launcher wallpapers and update titles."
  },
  "socials": {
    "url": "https://prod-alicdn-gamestarter.kurogame.com/...",
    "description": "Provides links to official social media channels."
  },
  "client_manifest": {
    "url": "https://prod-alicdn-gamestarter.kurogame.com/...",
    "description": "Contains manifests for game client downloads and repairs."
  }
}
```
### 2\. Versioned Files (e.g., `2.6.0v/*.json`)
The folders named after game versions (like `2.6.0v`) contain the **actual JSON data** returned by the APIs during that version's lifecycle.

  * `globalClient.json`: The game client manifest for downloading, updating, and repairing game files.
  * `news.json`: The raw data for news, events, and announcements shown in the launcher.
  * `socials.json`: The data for social media links and icons.
  * `wallpaper.json`: The data containing URLs for launcher background images and update titles.

-----

*Disclaimer: This is a community-driven project for archival and development purposes and is not officially affiliated with Kuro Games.*
