# ReproForge — releases

Public distribution channel for **ReproForge**, the findings-to-writeup
reporting tool for security testers. Built wheels are published here as GitHub
Releases (the source lives in a separate, private repo).

## Install

Requires Python 3.11+ and [pipx](https://pipx.pypa.io/). Install straight from
the release asset — replace the version with the one on the
[latest release](../../releases/latest) page:

```bash
pipx install https://github.com/malgo0/reproforge-releases/releases/download/v0.6.0/reproforge-0.6.0-py3-none-any.whl
reproforge            # starts the local web UI
```

(Or download the `.whl` first and `pipx install ./reproforge-<version>-py3-none-any.whl`.)

The tool checks this repo on startup and tells you when a newer version is
out; it never installs anything by itself. To upgrade, run the same
`pipx install --force <new wheel URL>` with the new version. Set
`REPROFORGE_NO_UPDATE_CHECK=1` to skip the check.

## Free vs Pro

The **free tier** — manual finding CRUD, full-text search, CVSS 3.1 builder,
Markdown export — works for everyone, no key needed. **Pro** (vulnerability
templates, AI-grounded repro steps, importers, delta reports) unlocks with a
license from **https://reproforge.com** ($35/month or $249/year, VAT included;
the key is shown right after checkout).

### Where the license key goes

Either of:

- the environment variable `REPROFORGE_LICENSE_KEY`, or
- the file `data/license.json` next to `data/findings.db` (in the directory
  you run ReproForge from), shaped `{"key": "your-key-here"}`.

The key is validated against `license.reproforge.com` (only the key string is
sent — never your findings) and cached, with a 3-day offline grace period.

## Support

- Lost key / billing / anything else: **hei@reproforge.com** (write from the
  e-mail address you bought with).
- Security issues: see https://reproforge.com/.well-known/security.txt
- Terms & refunds: https://reproforge.com/terms · Privacy: https://reproforge.com/privacy

## License

ReproForge is proprietary. These wheels are published so customers can install
and update the tool; the code is **not** licensed for reuse. See
https://reproforge.com.
