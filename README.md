🎵 TELEGRAM MUSIC & VIDEO DOWNLOADER BOT (RUST EDITION) 🦀

High-performance, reliable, and fast Telegram bot for searching, downloading, and processing music and videos. Written in Rust using the Teloxide framework, yt-dlp, and FFmpeg.

---


🔥 FEATURES

- 🔎 Fast Music Search: Searches up to 5 best tracks from YouTube by text query.
- 🎛️ On-the-fly Audio Effects (FFmpeg):
  - 🎵 Original (Clean 320 kbps quality)
  - 🌌 Slow + Reverb (Slowed down with ambient reverb)
  - ⚡ Nightcore (Speed up and pitched)
  - 🔊 Bass Boost (Heavy bass enhancement)
  - 🌀 8D Audio (Panning 8D stereo effect)
- 🔗 Direct Link Downloads: Supports TikTok, YouTube, and YouTube Shorts.
- 🎬 Format Selection: Download media as MP3 (Audio) or MP4 (Video).
- ⚡ High Performance:
  - Built-in LRU Cache for instant responses on frequent queries.
  - Fully asynchronous processing powered by tokio.
- 🛡️ Protection & Security:
  - Automatic anti-spam system (auto-bans users exceeding 5 requests per minute).
  - Blacklist support (ban.txt) by Telegram ID and @username.
  - Duration limit protection (ignores videos longer than 20 minutes).
  - Automatic temporary directory cleanup (temp_music).

---


🛠️ PREREQUISITES & DEPENDENCIES

Before running the bot, ensure you have the following installed on your system:


1. RUST TOOLCHAIN
Install Rust and Cargo via rustup:
* Linux/macOS:
    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
  
* Windows:
  Download and run rustup-init.exe from rustup.rs.


2. YT-DLP
yt-dlp must be installed and added to your system's PATH.
* Linux (Ubuntu/Debian):
    sudo wget https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -O /usr/local/bin/yt-dlp
  sudo chmod a+rx /usr/local/bin/yt-dlp
  
* macOS (via Homebrew):
    brew install yt-dlp
  
* Windows (via winget):
    winget install yt-dlp
  
  *(Or download executable manually from yt-dlp GitHub Releases and add to PATH)*


3. FFMPEG
FFmpeg must be installed and added to your system's PATH.
* Linux (Ubuntu/Debian):
    sudo apt update && sudo apt install ffmpeg -y
  
* macOS (via Homebrew):
    brew install ffmpeg
  
* Windows (via winget):
    winget install Gyan.FFmpeg
  
  *(Or download builds from ffmpeg.org and add bin folder to system PATH)*

---


🚀 INSTALLATION & SETUP


1. CLONE THE REPOSITORY
git clone https://github.com/Catonymous2010/telegram-musicbot.git
cd telegram-musicbot



2. CONFIGURE ENVIRONMENT VARIABLES
Create a .env file in the root directory of the project:
touch .env

Add your Telegram Bot Token received from @BotFather:
BOT_TOKEN=your_telegram_bot_token_here



3. BUILD AND RUN


DEVELOPMENT MODE:
cargo run



PRODUCTION MODE (MAX PERFORMANCE):
cargo build --release
./target/release/telegram-musicbot

*(On Windows: .\target\release\telegram-musicbot.exe)*

---


📁 SYSTEM FILES STRUCTURE

The bot automatically creates and manages the following files at runtime:
– temp_music/ — Temporary directory for downloads and processing (automatically cleared on startup).
– log.txt — Detailed runtime activity and event logs.
– ban.txt — List of blocked users (by ID or @username).
– users.txt — Registered database of unique bot users.

---


👤 AUTHOR

– Developer: Catonymous2010
– Language: Rust 🦀    
