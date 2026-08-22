# ReproForge — releases

Public distribution channel for **ReproForge**, the findings-to-writeup
reporting tool for security testers. Built wheels are published here as GitHub
Releases (the source lives in a separate, private repo).

## Install

Download the wheel from the [latest release](../../releases/latest) and:

```bash
pipx install ./reproforge-<version>-py3-none-any.whl
reproforge
```

First run walks you through pasting a license key (optional — the free tier
works without one) and choosing an AI provider (bring your own key). Update
later with `pipx upgrade reproforge` (the tool also checks here on startup and
tells you when a new version is out).

## Free vs Pro

The **free tier** — manual finding CRUD, full-text search, CVSS 3.1 builder,
Markdown export — works for everyone. **Pro** (vulnerability templates,
AI-grounded repro steps, importers) unlocks with a license from
**https://reproforge.com**.

## License

ReproForge is proprietary. These wheels are published so customers can install
and auto-update the tool; the code is **not** licensed for reuse. See
https://reproforge.com.
