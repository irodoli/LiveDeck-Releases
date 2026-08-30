# LiveDeck Releases

Official public **update-only** channel for already-installed LiveDeck clients.

## Initial installation / recovery

The latest Windows Full Setup is distributed only through the owner's protected download portal at `https://dl.irodoli.com/`. This repository is not a Full Setup download route.

## Legacy clients -> current Full bridge

LiveDeck builds before v0.8.8 use the retired signed Full-update contract and do not read the new delta channel. Those clients must install the protected **latest Full Setup** once from `https://dl.irodoli.com/` to enter the delta-update line (currently v0.8.9). Do not expect a pre-v0.8.8 client to discover the bridge/latest release through `delta-latest.json`.

## Delta updates (v0.8.8+)

LiveDeck v0.8.8 is the baseline/bridge into the new delta updater. v0.8.8+ clients read the signed `delta-latest.json` channel from this repository. The current Stable target is v0.8.9 with one exact v0.8.8 -> v0.8.9 delta step. Future update publication consists of:

- delta package(s)
- signed `delta-latest.json`
- `RELEASE_NOTES.txt`

New post-bridge releases must not add a Full Setup, full application payload, or Source ZIP to GitHub. The client verifies the signed manifest, exact source Version/Build ID, package SHA-256/size, complete base/final file manifests, and a staged health-check before safe replacement with rollback.

If an installed v0.8.8+ client has no supported delta chain, its base files do not match, or verification/health-check fails, LiveDeck directs the user to the protected Full Setup at `https://dl.irodoli.com/`; it does not fetch a GitHub Full.

## Legacy assets

Older GitHub Release Full Setup assets are retained only as historical compatibility assets. They are not the current publication model and do not provide the current Full bridge for pre-v0.8.8 clients.

The LiveDeck source code, signing private key, credentials, user data, and unrelated development artifacts are not published here.
