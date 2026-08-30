# LiveDeck Releases

Official public **update-only** channel for already-installed LiveDeck clients.

## Initial installation / recovery

The latest Windows Full Setup is distributed only through the owner's protected download portal at `https://dl.irodoli.com/`. This repository is not a Full Setup download route.

## Delta updates (v0.8.8+)

LiveDeck v0.8.8 is the bridge release. New clients read the signed `delta-latest.json` channel from this repository. Future update publication consists of:

- delta package(s)
- signed `delta-latest.json`
- `RELEASE_NOTES.txt`

New releases must not add a Full Setup, full application payload, or Source ZIP to GitHub. The client verifies the signed manifest, exact source Version/Build ID, package SHA-256/size, complete base/final file manifests, and a staged health-check before safe replacement with rollback.

If an installed client has no supported delta chain, its base files do not match, or verification/health-check fails, LiveDeck directs the user to the protected Full Setup at `https://dl.irodoli.com/`; it does not fetch a GitHub Full.

## Legacy assets

Older GitHub Release Full Setup assets are retained only while required for compatibility with already-installed legacy clients. They are historical compatibility assets and are not the current publication model.

The LiveDeck source code, signing private key, credentials, user data, and unrelated development artifacts are not published here.
