# Wuwa-Web-Request
A repository for archiving the Web Request/JSON data responses from the official *Wuthering Waves* launcher and game client APIs.

Maintained by [Acheuy](https://github.com/Cheu3172).

## Repository Structure
This repository is organized by game/launcher version. Each version has its own dedicated folder containing the JSON data relevant to that specific release.

```
.
├── api.json
├── 2.6.0v/
│   ├── news-notices.json
│   ├── osLive-client.json
│   ├── osLive-localpath-index.json
│   ├── osBeta-client.json (if available)
│   ├── cnLive-client.json
│   ├── cnLive-localpath-index.json
│   ├── cnBeta-client.json (if available)
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
  "clients": {
    "osLive": {
      "client": {
        "url": "https://prod-alicdn-gamestarter.kurogame.com/launcher/game/G153/50004_obOHXFrFanqsaIEOmuKroCcbZkQRBC7c/index.json",
        "description": "Provides an index of data used in Downloading & Updating the game in the Official Launcher."
      },
      "news-notices": {
        "url": "https://prod-alicdn-gamestarter.kurogame.com/launcher/50004_obOHXFrFanqsaIEOmuKroCcbZkQRBC7c/G153/information/en.json",
        "description": "Provides the content for the News Content Section in the Official Launcher."
      },
      "wallpapers-slogan": {
        "url": "https://prod-alicdn-gamestarter.kurogame.com/launcher/50004_obOHXFrFanqsaIEOmuKroCcbZkQRBC7c/G153/background/U82Wn9dbNc2o7zZBWz1cOnJm9r52qFKH/en.json?_t=1758743410",
        "description": "Provides the content for the version Wallpaper & Slogan in the Official Launcher."
      },
      "socials-icons": {
        "url": "https://prod-alicdn-gamestarter.kurogame.com/launcher/G153/50004_obOHXFrFanqsaIEOmuKroCcbZkQRBC7c/social/en.json?_t=1758744184",
        "description": "Provides the content for the Socials Section in the Official Launcher."
      },
      "localpath-index": {
        "url": "https://hw-pcdownload-qcloud.aki-game.net/launcher/game/G153/50004/2.6.2/TmryWWDzYshLRahsXoGizseCUnInEDtj/resource/50004/2.6.2/indexFile.json",
        "description": "Provides an indexFile of localpaths for checking osLive file integrity, used in the Official Launcher for repairs."
      }
    },
    "osBeta": {
      "client": {
        "url": "https://prod-alicdn-gamestarter.kurogame.com/launcher/game/G153/50013_HiDX7UaJOXpKl3pigJwVxhg5z1wllus5/index.json",
        "description": "Provides an index of data used in Downloading & Updating the game in the Official Launcher, for overseas beta client."
      }
    },
    "cnLive": {
      "client": {
        "url": "https://prod-cn-alicdn-gamestarter.kurogame.com/launcher/game/G152/10003_Y8xXrXk65DqFHEDgApn3cpK5lfczpFx5/index.json",
        "description": "Provides an index of data used in Downloading & Updating the game in the Official Launcher, for China live client."
      },
      "localpath-index": {
        "url": "https://pcdownload-aliyun.aki-game.com/launcher/game/G152/10003/2.6.2/DYINNoSACrMDUahXEhMxmWqVOHJjvFSH/resource/10003/2.6.2/indexFile.json",
        "description": "Provides an indexFile of localpaths for checking cnLive file integrity, used in the Official Launcher for repairs."
      }
    },
    "cnBeta": {
      "client": {
        "url": "https://prod-cn-alicdn-gamestarter.kurogame.com/launcher/game/G152/10008_Pa0Q0EMFxukjEqX33pF9Uyvdc8MaGPSz/index.json",
        "description": "Provides an index of data used in Downloading & Updating the game in the Official Launcher, for China beta client."
      }
    }
  }
}
```
### 2\. Versioned Files (e.g., `2.6.0v/*.json`)
The folders named after game versions (like `2.6.0v`) contain the **actual JSON data** returned by the APIs during that version's lifecycle.

  * `osLive-localpath-index.json` The data of localpaths, usually used when running repair in the launcher, only for osLive.
  * `cnLive-localpath-index.json` The data of localpaths, usually used when running repair in the launcher, only for cnLive.
  * `news-notices.json`: The data for news, notices, and banners shown in the launcher, only for osLive.
  * `socials-icons.json`: The data containing URLs for launcher background images and update titles, only for osLive.
  * `wallpapers-slogan.json`: The data for the Launcher's version wallpaper, and slogan, only for osLive.
  * `osLive-client.json`: The data for osLive Downloads & Updates, also other info.
  * `osBeta-client.json`: The data for osBeta Downloads & Updates, also other info. (if available)
  * `cnLive-client.json`: The data for cnLive Downloads & Updates, also other info.
  * `cnBeta-client.json`: The data for cnBeta Downloads & Updates, also other info. (if available)

-----

*Disclaimer: This is a community-driven project for archival and development purposes and is not officially affiliated with Kuro Games.*
