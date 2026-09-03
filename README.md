# PeoplesHR Bug Fixer — update feed

This repository is the update feed for the **PeoplesHR Bug Fixer** desktop application. It is
consumed by the application itself, not by people.

- `latest.json` — the current release: version, size and SHA-256 of the payload.
- `payloads/<version>.bin` — that release, encrypted (AES-256-GCM). Nothing here is
  human-readable, and the application verifies the hash before it decrypts anything.

It is public for one reason only: the application then reads the feed over plain HTTPS with no
credential, which keeps it working on any network and avoids per-office API rate limits.

Issues and pull requests are not monitored here.
