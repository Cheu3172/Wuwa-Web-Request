# Wuwa-Web-Request
A repository for archiving the Web Request/JSON data responses from the official *Wuthering Waves* launcher and game client APIs.

Maintained by [Acheuy](https://github.com/Cheu3172).
## Repository Structure
This repository is organized by game/launcher version. Each version has its own dedicated folder containing the JSON data relevant to that specific release.

```
.
├── api.json
├── 2.6.0v/
│   ├── localpath-index.json
│   ├── news-notices.json
│   ├── osLive-client.json
│   ├── socials-icons.json
│   └── wallpapers-slogan.json
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
  "news-notices": {
    "url": "https://prod-alicdn-gamestarter.kurogame.com/launcher/50004_obOHXFrFanqsaIEOmuKroCcbZkQRBC7c/G153/information/en.json",
    "description": "Provides the content for the News Content Section in the Official Launcher."
  },
  "wallpapers-slogan": {
    "url": "https://prod-alicdn-gamestarter.kurogame.com/launcher/50004_obOHXFrFanqsaIEOmuKroCcbZkQRBC7c/G153/background/U82Wn9dbNc2o7zZBWz1cOnJm9r52qFKH/en.json?_t=1758743410",
    "description": "Provides the content for the version Wallpaper & Slogan in the Offical Launcher."
  },
  "socials-icons": {
    "url": "https://prod-alicdn-gamestarter.kurogame.com/launcher/G153/50004_obOHXFrFanqsaIEOmuKroCcbZkQRBC7c/social/en.json?_t=1758744184",
    "description": "Provides the content for the Socials Section in the Official Launcher."
  },
  "localpath-index": {
    "url": "https://hw-pcdownload-qcloud.aki-game.net/launcher/game/G153/50004/[VERSION HERE(Example: 2.6.2)]/TmryWWDzYshLRahsXoGizseCUnInEDtj/resource/50004/2.6.2/indexFile.json",
    "description": "Provides an indexFile of localpaths for checking osLive file integrity, used in the Official Launcher for repairs."
  },
  "osLive-client": {
    "url": "https://prod-alicdn-gamestarter.kurogame.com/launcher/game/G153/50004_obOHXFrFanqsaIEOmuKroCcbZkQRBC7c/index.json",
    "description": "Provides an index of data used in Downloading & Updating the game in the Official Launcher, for overseas live client."
  }
}
```
### 2\. Versioned Files (e.g., `2.6.0v/*.json`)
The folders named after game versions (like `2.6.0v`) contain the **actual JSON data** returned by the APIs during that version's lifecycle.

  * `localpath-index.json` The data of localpaths, usually used when running repair in the launcher.
  * `news-notices.json`: The data for news, notices, and banners shown in the launcher.
  * `osLive-client.json`: The data for Downloads & Updates, also other info.
  * `socials-icons.json`: The data containing URLs for launcher background images and update titles.
  * `wallpapers-slogan.json`: The data for the Launcher's version wallpaper, and slogan.

-----

*Disclaimer: This is a community-driven project for archival and development purposes and is not officially affiliated with Kuro Games.*
