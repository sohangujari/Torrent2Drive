# 🧲 Torrent2Drive

> Download torrents directly to your Google Drive using Google Colab - no local storage needed.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/sohangujari/Torrent2Drive/blob/main/Torrent2Drive.ipynb)
![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-F9AB00?logo=googlecolab)

---

## ⚠️ Disclaimer

> **This tool is intended for downloading legal and authorized content only.**
> The author is **not responsible** for any misuse of this tool.
> Downloading copyrighted material without permission is **illegal** in most jurisdictions.
> By using this tool, you agree that **you are solely responsible** for the content you download.
> Please respect copyright laws in your country.

---

## 📖 About

**Torrent2Drive** is a lightweight Google Colab notebook that lets you download torrents (via **magnet links** or **`.torrent` files**) and save them directly to your **Google Drive**. No local bandwidth, no local storage - everything runs in the cloud.

---

## ✨ Features

- 🧲 **Magnet link & `.torrent` file** support
- ☁️ **Direct to Google Drive** - no local disk needed
- 📊 **Real-time progress** - speed, ETA, peers, state
- ⚡ **Optimized session** - DHT, LSD, NAT-PMP, UPnP enabled
- 🧩 **Smart piece prioritization** - first & last pieces downloaded first
- 🔒 **Sparse storage mode** - efficient disk usage
- 🧹 **Graceful cleanup** on interruption

---

## 🚀 Quick Start

### Option 1: One-Click (Recommended)

Click the badge below to open directly in Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/Torrent2Drive/blob/main/Torrent2Drive.ipynb)

### Option 2: Manual Setup

1. Open [Google Colab](https://colab.research.google.com/)
2. Go to `File` → `Open Notebook` → `GitHub`
3. Paste this repo URL and open `Torrent2Drive.ipynb`

---

## 📋 Usage

### Step 1 - Install dependency
Run the first cell to install `libtorrent`:
!pip install libtorrent

### Step 2 - Run the downloader
Run the second cell. It will:
1. Mount your Google Drive
2. Ask for a **magnet link** or **`.torrent` file path**
3. Start downloading with live progress

### Step 3 - Enter your torrent source
Magnet link or .torrent file path: magnet:?xt=urn:btih:XXXX...

### Step 4 - Watch the progress
45.23% ↓ 1234.5 kB/s ↑ 56.7 kB/s Peers: 42 ETA: 0:12:34 [Downloading]

### Step 5 - Find your files
Downloaded files are saved to:
Google Drive → My Drive → Torrent

---

## 📁 Project Structure

```
Torrent2Drive/
├── Torrent2Drive.ipynb
└── README.md
```

---

## ⚙️ Configuration

You can customize these settings in the notebook:

| Setting | Default | Description |
|---|---|---|
| `DOWNLOAD_FOLDER` | `/content/drive/My Drive/Torrent` | Save location on Drive |
| `upload_rate_limit` | `10 MB/s` | Upload speed limit |
| `download_rate_limit` | `0` (unlimited) | Download speed limit |
| `active_downloads` | `5` | Max concurrent downloads |
| `METADATA_TIMEOUT` | `120s` | Timeout for fetching metadata |

---

## 📸 Preview

```
⏳ Fetching metadata... done.

──────────────────────────────────────────────────────
📦 Ubuntu-24.04-desktop-amd64.iso
💾 Size   : 5.74 GB (6,163,578,880 bytes)
🧩 Pieces : 5878 × 1024 KB
📁 Saving : /content/drive/My Drive/Torrent
──────────────────────────────────────────────────────

100.00% ↓ 0.0 kB/s ↑ 0.0 kB/s Peers: 0 ETA: 0:00:00 [Seeding]

✅ Done in 0:15:32 → /content/drive/My Drive/Torrent
```

---

## ⚠️ Limitations

| Limitation | Details |
|---|---|
| ⏱️ **Colab timeout** | Free tier disconnects after ~90 min of inactivity |
| 💾 **Drive storage** | Limited by your Google Drive quota (15 GB free) |
| 🔄 **Session reset** | Colab runtime resets - re-run cells after disconnect |
| 📦 **Large files** | Very large torrents may exceed Colab's temp storage |

---

## 💡 Tips

- 🖱️ **Keep the tab active** to prevent Colab from disconnecting
- 📂 **Change save folder** by editing `DOWNLOAD_FOLDER`
- 🛑 **Stop anytime** - use `Ctrl+C` or interrupt the cell; cleanup runs automatically
- 🔗 **Use magnet links** - no need to upload `.torrent` files

---

## 🛠️ Tech Stack

- [Google Colab](https://colab.research.google.com/) - Free cloud runtime
- [libtorrent](https://libtorrent.org/) - High-performance BitTorrent library
- [Python 3](https://python.org/) - Programming language
- [Google Drive API](https://developers.google.com/drive) - Cloud storage

---

## ⭐ Support

If you found this useful, give it a ⭐ on GitHub!
