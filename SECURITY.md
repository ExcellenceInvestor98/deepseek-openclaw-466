# Security Policy

## Reporting a Vulnerability

Please open a private security advisory or contact the repository maintainer directly.
Do not disclose exploitable issues publicly before a fix is available.

## Secret Handling

This project is designed as a local-first configuration assistant. API keys typed into the UI are used only in the current browser session and are not sent to any server by this app.

Recommended practices:

- Do not commit `.env`, API keys, session files, or local OpenClaw configuration files containing secrets.
- Prefer environment variables or OpenClaw auth profiles for credentials.
- Keep OpenClaw channel allowlists strict when exposing the assistant to messaging platforms.
- Review generated configuration before copying it into a real OpenClaw setup.
