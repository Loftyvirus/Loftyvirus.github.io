---
title: VLC-Discord RPC
description: VLC media player rich presence for Discord
layout: libdoc/page
order: 1
---


A simple integration that updates your Discord status with the media currently playing on **VLC Media Player** using Discord's Rich Presence.

## Features

- Auto-detects VLC activity.
- Updates Discord status with media details.
- Supports major media formats (`.mkv`, `.mp4`, `.avi`, `.mov`, `.mp3`, `.flac`, `.wav`).
- Simple setup and usage.

## Installation

### Prerequisites

- Python 3.7+
- VLC Media Player
- A Discord application with Rich Presence enabled (`CLIENT_ID` required)

### Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Loftyvirus/VLC-discord-RPC
   cd vlc-discord-rpc
   ```
2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Set up `.env` file:**
   ```bash
   cp config/.env.example config/.env
   ```
   Edit `config/.env` to add your Discord `CLIENT_ID`:
   ```
   CLIENT_ID=your_discord_client_id_here
   ```
4. **Run the application:**
   ```bash
   python main.py
   ```

## Usage

1. Start VLC and play a media file.
2. Run the application (`python main.py`).
3. Discord status updates automatically.
4. Press `Ctrl+C` to stop.

## Configuration

- `CLIENT_ID`: Required for Discord Rich Presence ([Create one](https://discord.com/developers/applications)).

## Contributing

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/YourFeatureName`).
3. Commit changes (`git commit -m 'Add feature'`).
4. Push (`git push origin feature/YourFeatureName`).
5. Open a pull request.

## Acknowledgments

- [pypresence](https://github.com/qwertyquerty/pypresence) - Discord Rich Presence library.
- [psutil](https://github.com/giampaolo/psutil) - Process monitoring.
- [python-dotenv](https://github.com/theskumar/python-dotenv) - Environment variable management.
