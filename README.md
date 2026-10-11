# clinical-ai-disclosure-landing

Static landing site for the **[Clinical AI Disclosure spec](https://github.com/mizcausevic-dev/clinical-ai-disclosure-spec)** — the HealthTech vertical extension to the [Kinetic Gain Protocol Suite](https://github.com/mizcausevic-dev/kinetic-gain-protocol-suite).

Live at **[clinical.kineticgain.com](https://clinical.kineticgain.com)**.

## What's here

```
.
├── index.html              # the landing page
├── style.css               # styles (medical-blue + slate palette)
├── .github/workflows/
│   └── deploy.yml          # manual GitHub Actions upload (currently unverified)
└── README.md
```

No build step. Hand-written HTML + CSS so the page loads instantly and degrades cleanly without JS.

## Local preview

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Deployment

Merging to `main` does not deploy. The GitHub Actions upload runs only on `workflow_dispatch`; its FTPS path is unverified. For a release, use the reviewed local Hostinger SSH/SFTP route with a pinned host key, exact file backups and hashes, hosted checks, and a tested restore.

Secrets required only for the manually dispatched Actions upload:

| Secret | Description |
|---|---|
| `FTP_HOST` | Hostinger FTP server hostname |
| `FTP_USER` | Hostinger FTP username |
| `FTP_PASS` | Hostinger FTP password |

(Same values as `aeo-visualizer`, `ai-tutor-cards-landing`, `prompt-injection-bench-web`.)

## Related repositories

- **[clinical-ai-disclosure-spec](https://github.com/mizcausevic-dev/clinical-ai-disclosure-spec)** — the specification, JSON Schema, and canonical examples
- **[kinetic-gain-visualizer](https://github.com/mizcausevic-dev/kinetic-gain-visualizer)** — visualizer for supported Suite documents
- **[mcp-kinetic-gain](https://github.com/mizcausevic-dev/mcp-kinetic-gain)** — unified MCP server

## License

Apache-2.0 for this site. The underlying specification is MIT-licensed.
