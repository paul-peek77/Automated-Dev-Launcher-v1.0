# Automated Dev Launcher, v1.0 (ADL)

A cross‑platform development environment orchestrator

---

This project is provided for portfolio review only. No permission is granted for reuse, modification, or redistribution.

---

Overview

The Automated Dev Launcher (ADL) is a workflow automation tool designed to streamline complex multi‑service development environments. It coordinates:

- Node/NVM setup
- Firebase Emulator Suite
- Vite development server
- Stripe CLI webhook forwarding
- Log monitoring
- Chrome app‑mode launch
- Automatic cleanup on exit

The launcher is built for environments where multiple services must start in a specific order and remain synchronized during development.

This repo contains:

- the launcher scripts
- a minimal placeholder project structure
- a site‑map example
- documentation explaining how to adapt the launcher to real projects

No proprietary source code is included.

---

Features

🔥 Environment Orchestration

- Ensures correct Node version via NVM
- Loads environment variables securely
- Cleans up stale processes and ports

🧱 Multi‑Service Startup

- Starts Firebase emulators in a tmux session
- Waits until all emulators are fully ready
- Launches Vite frontend
- Launches Stripe CLI listener
- Opens a live log window

🧹 Automatic Cleanup

When the Chrome app window closes:

- all tmux sessions terminate
- all dev processes shut down
- temporary Chrome profile is removed

🖥️ Developer Experience

- One‑click .desktop launcher (Linux)
- Wrapper script for GUI environments
- Headless mode for terminal‑only workflows

---

Repository Structure

Below is the repo layout using clean spacing (no markdown box):

    Automated-Dev-Launcher/
        launcher/
            pimpire-gauntlet.sh
            pimpire-gauntlet-wrapper.sh
            Pimpire Gauntlet.desktop
        example-project/
            client/
                package.json.example
            functions/
                .env.example
            firebase.json.example
            README.md
        site-map.txt
        .gitignore
        README.md

---

Placeholder Project Structure

This placeholder exists solely to demonstrate the expected layout of a real project. It contains no functional code and no proprietary logic.

    example-project/
        client/
            package.json.example
        functions/
            .env.example
        firebase.json.example
        README.md

Why this exists

The launcher expects certain directories and files to exist.
This placeholder shows the structure without exposing any real implementation.

---

Site Map Example

A simple site‑map is included to illustrate the intended project shape:

    001 ./client/package.json
    002 ./client/src/...
    003 ./functions/index.js
    004 ./firebase.json
    005 ./firestore.rules

This is for demonstration only.

---

Usage

1. Make the launcher executable
`
chmod +x launcher/pimpire-gauntlet.sh
chmod +x launcher/pimpire-gauntlet-wrapper.sh
`

2. Adjust paths
Edit the launcher script to point to your real project directory:

`
PROJECT_DIR="/path/to/your/project"
CLIENTDIR="$PROJECTDIR/client"
`

3. Provide your own environment variables
Copy .env.example to .env inside your real project.

4. Run the launcher
`
./launcher/pimpire-gauntlet.sh
`

Or use the .desktop file on Linux for a one‑click launch.

---

Dependencies

- Node.js (via NVM)
- Firebase CLI
- Stripe CLI
- tmux
- Google Chrome
- Bash (Linux)

---

Limitations

- Placeholder project is non‑functional
- No proprietary code is included
- Launcher assumes a Linux environment (WSL compatible)

---

Purpose

This repo demonstrates:

- environment orchestration
- process management
- developer tooling
- cross‑service synchronization
- automation design

It is part of a larger portfolio showcasing systems engineering and workflow automation.
