# Auto-Recon-Bot

## Overview

**Auto-Recon-Bot** is an integrated toolkit for automated web security reconnaissance and vulnerability evaluation, combining Python orchestration (with Telegram integration) and a series of modular Bash scripts. This tool allows penetration testers, bug bounty hunters, and DevSecOps professionals to run advanced asset discovery, vulnerability scans, and reporting operations—all controlled via a Telegram bot for real-time interaction and notifications.

## Features

- **Telegram bot interface:** Easily control and receive real-time scan results.
- **Automated orchestration:** Runs subdomain enumeration, XSS, SSRF, clickjacking, port scanning, and more.
- **Modular architecture:** Add new Bash/command-line scripts for extra checks.
- **Real-time log delivery:** Get results and detailed logs via Telegram chat.
- **Audit logging:** Full tracking of bot actions and scan results.

## Architecture

- `bot.py`: Telegram bot controller; authenticates users, receives scan commands, orchestrates modules, sends results/logs via Telegram.
- `run.py`: Orchestrates a sequence of scans on a target domain/URL and sends status updates to Telegram.
- `Aptfile`: System package dependencies for cloud/Docker/Heroku deployment.
- `requirements.txt`: Python package dependencies.
- **Modules (Bash scripts)**:
- Examples: `recon.sh`, `Subdomain_Enum.sh`, `Portscan_Fast.sh`, `robots.sh`, etc.
- `bot.log`: Stores audit logs of bot actions and results.

## Usage

### Installation

**Install system dependencies**
```bash
sudo apt-get update
sudo apt-get install <packages listed in Aptfile>
```

**Install Python dependencies**
```bash
pip install -r requirements.txt
```

**Configure Telegram credentials**
- Set your Telegram Bot API key and authorized usernames in the config file (YAML or environment variables).

### Running the Suite

**Start bot**
```bash
python bot.py
```
**Or run scanner directly**
```bash
python run.py <target-domain>
```

**Control via Telegram**
- Send commands through Telegram chat:
- `/subdomain`
- `/portscan`
- `/getlog`
- ...and others
- Receive scan results, notification updates, download logs and outputs.
## Contributing

1. Fork this repository.
2. Open an issue to discuss features or improvements.
3. Submit a pull request with a clear description.
4. Ensure new modules/scripts follow the established format and generate logs/results for Telegram delivery.

## License

Dedicated to the public domain under the CC0 license.

https://github.com/user-attachments/assets/40484fd9-6f10-4a17-8c4a-695e3fffc93e

