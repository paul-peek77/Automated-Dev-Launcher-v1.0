# Automated Dev Launcher, v1.0

This project is provided for portfolio review only. No permission is granted for reuse, modification, or redistribution.

OVERVIEW

The Multi‑Terminal Dev Environment Launcher automates the startup and shutdown of a three‑server development environment using Python, PowerShell, and tmux. It launches backend, frontend, and Stripe listener processes in coordinated terminal sessions, opens the local web app in the browser, and automatically shuts everything down when the browser closes.

This project demonstrates:
- multi‑process orchestration
- tmux session management
- cross‑platform scripting
- developer workflow automation
- safe startup and teardown logic

KEY FEATURES

- Automated multi‑server startup — backend, frontend, and Stripe listener
- tmux‑based orchestration — clean, isolated terminal sessions
- Automatic cleanup — shuts down all processes when the browser closes
- Cross‑platform support — Python + PowerShell
- Developer‑friendly workflow — one command to start everything

PURPOSE

This tool was built to streamline local development workflows and reduce manual setup steps. It also serves as a demonstration of automation engineering, process lifecycle management, and developer tooling design.
