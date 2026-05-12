# clinical-ai-disclosure-landing

Static landing site for the **[Clinical AI Disclosure spec](https://github.com/mizcausevic-dev/clinical-ai-disclosure-spec)** — the HealthTech vertical extension to the [Kinetic Gain Protocol Suite](https://github.com/mizcausevic-dev/kinetic-gain-protocol-suite).

Live at **[clinical.kineticgain.com](https://clinical.kineticgain.com)**.

## What's here

```
.
├── index.html              # the landing page
├── style.css               # styles (medical-blue + slate palette)
├── .github/workflows/
│   └── deploy.yml          # FTPS push to /clinical/ on Hostinger on push to main
└── README.md
```

No build step. Hand-written HTML + CSS so the page loads instantly and degrades cleanly without JS.

## Local preview

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Deployment

Pushes to `main` trigger a GitHub Actions workflow that FTP-syncs the site root to `/clinical/` on Hostinger.

Required repo secrets:

| Secret | Description |
|---|---|
| `FTP_HOST` | Hostinger FTP server hostname |
| `FTP_USER` | Hostinger FTP username |
| `FTP_PASS` | Hostinger FTP password |

(Same values as `aeo-visualizer`, `ai-tutor-cards-landing`, `prompt-injection-bench-web`.)

## Related repositories

- **[clinical-ai-disclosure-spec](https://github.com/mizcausevic-dev/clinical-ai-disclosure-spec)** — the specification, JSON Schema, and canonical examples
- **[kinetic-gain-visualizer](https://github.com/mizcausevic-dev/kinetic-gain-visualizer)** — unified visualizer for all 10 specs
- **[mcp-kinetic-gain](https://github.com/mizcausevic-dev/mcp-kinetic-gain)** — unified MCP server

## License

Apache-2.0. The underlying specification is AGPL-3.0.
