# 🤖 tp-computer-use-agent: Autonomous Computer-Use & OS Operator Agent Studio

Production implementation of the **Anthropic Computer Use API** (Claude 3.5 Sonnet) operating inside containerized X11/Xvfb virtual desktop sandboxes.

🔗 **Interactive Studio:** [talaripradeep.info/tools/computer-use-agent/](https://talaripradeep.info/tools/computer-use-agent/)

![Computer Use Agent Flow](docs/computer_use_flow.png)

## Overview

Enables AI agents to interact with graphical desktop interfaces just like humans: capturing screen states, grounding coordinates, moving mouse cursors, typing keystrokes, and executing GUI workflows.

## Key Features

- **X11 / Xvfb Virtual Framebuffer**: Runs headless GUI desktops (1920x1080) inside isolated Docker containers.
- **Human-in-the-Loop Gatekeeper**: Requires explicit operator approval before executing high-risk bash commands or sensitive network transactions.
- **Coordinate Grounding**: Normalizes screenshot resolutions and maps token predictions to exact pixel coordinates.
- **Audit Logging**: Captures full video frames and action traces for SOC2 and security audits.

## Quickstart

```bash
docker build -t computer-use-sandbox -f Dockerfile.sandbox .
docker run -it -p 5900:5900 computer-use-sandbox
```

## License

MIT © 2026 Talari Pradeep
