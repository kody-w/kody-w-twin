# @kody-w's twin

Front door for @kody-w's digital twin. Planted via the RAPP public-tether flow on 2026-05-11.

- **Rappid:** `rappid:v2:operator:@kody-w/twin:5b8ba4796692197aa4ccde5dfa5beb51@github.com/kody-w/kody-w-twin`
- **Live:** https://kody-w.github.io/kody-w-twin/
- **Parent species:** [kody-w/RAPP](https://github.com/kody-w/RAPP)

## What this repo is

Per CONSTITUTION Article XLVI, every operator's rappid IS their global address — and the rappid resolves to a GitHub-hosted front door. This repo is that door for @kody-w. Other operators who want to address @kody-w dial this address from any tether.

Conforms to **Article LI** (front-gate QR mandatory): `index.html` includes the canonical `rapp-front-gate-qr/1.0` snippet (QRious + jsdelivr, graceful degrade).

## What's in here

| File | Purpose |
|---|---|
| `rappid.json` | The operator's permanent v2 rappid (Article XLVI). |
| `soul.md` | Twin persona — the system prompt that any brainstem hosting this twin uses. |
| `members.json` | Trivial — just the operator (this is a personal twin, not a neighborhood). |
| `index.html` | Public front gate with the Article-LI tether QR. |
| `.well-known/twin.egg` | The brainstem-egg invite cartridge — scan or paste this URL into any tether to address this twin. |
| `.nojekyll` | Tell GitHub Pages not to Jekyll-process. |
