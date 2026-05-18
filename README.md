# @kody-w's twin

> The operator twin for @kody-w.  Both a public front door (per
> CONSTITUTION Article XLVI + LI) **and** a hatchable twin identity.

- **Rappid:** `rappid:v2:operator:@kody-w/twin:5b8ba4796692197aa4ccde5dfa5beb51@github.com/kody-w/kody-w-twin`
- **Live front door:** https://kody-w.github.io/kody-w-twin/
- **Parent species:** [`kody-w/RAPP`](https://github.com/kody-w/RAPP)

## Two uses for this repo

### 1. Public front door (Article XLVI + LI)

Every operator's rappid IS their global address, and that rappid
resolves to a GitHub-hosted front door.  This repo is that door for
@kody-w; other operators dial it from any tether.

| File | Purpose |
|------|---------|
| `rappid.json` | Operator's permanent v2 rappid (Article XLVI). |
| `soul.md` | Twin persona — system prompt for any brainstem hosting this twin. |
| `members.json` | Trivial — just the operator. |
| `index.html` | Public front gate with the canonical `rapp-front-gate-qr/1.0` snippet (Article LI). |
| `.well-known/twin.egg` | Brainstem-egg invite cartridge. |
| `.nojekyll` | Tell GitHub Pages not to Jekyll-process. |

### 2. Hatchable twin — bring @kody-w local

This repo carries *only* the twin's identity.  The hatcher itself
lives at
[`kody-w/twin-egg-hatcher`](https://github.com/kody-w/twin-egg-hatcher)
(public mirror of `kody-w/aibast-twin`, private canonical).  One
generic hatcher for every twin — no copy-paste-drift.

**One-liner — fetch the hatcher, then hatch this twin:**

```bash
# 1. fetch the generic hatcher into the current folder
curl -fsSL https://raw.githubusercontent.com/kody-w/kody-w-twin/main/install.sh | bash

# 2. hatch @kody-w's twin (pulls identity from this repo's main branch)
python ./twin_egg_hatcher_agent.py hatch --source kody-w/kody-w-twin
```

Or, if you cloned this repo already:

```bash
gh repo clone kody-w/kody-w-twin && cd kody-w-twin
curl -fsSL https://raw.githubusercontent.com/kody-w/twin-egg-hatcher/main/install.sh | bash
python ./twin_egg_hatcher_agent.py hatch           # auto-detects from cwd
```

**Federate through the global brainstem:**

```
> Twin(action="list")                                                # see this twin
> Twin(action="boot",  rappid_uuid="rappid:v2:operator:@kody-w/...")  # start on a free port
> Twin(action="chat",  rappid_uuid="rappid:v2:operator:@kody-w/...", message="hi Kody")
```

The global brainstem source is never touched in the default flow.

## Pattern lineage

| Concern | Where it lives |
|---------|----------------|
| Twin identity (rappid, soul, agents) | this repo |
| Generic hatcher (one file, any twin) | [`kody-w/twin-egg-hatcher`](https://github.com/kody-w/twin-egg-hatcher) (public mirror) · [`kody-w/aibast-twin`](https://github.com/kody-w/aibast-twin) (private canonical) |
| Global brainstem + `Twin` federation agent | [`kody-w/rapp-installer`](https://github.com/kody-w/rapp-installer) |
| Constitution (Articles XLVI front-door, LI QR-gate) | [`kody-w/RAPP`](https://github.com/kody-w/RAPP) |

Conforms to **Article LI** (front-gate QR mandatory): `index.html`
includes the canonical `rapp-front-gate-qr/1.0` snippet.
