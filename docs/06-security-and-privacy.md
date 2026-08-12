# 06 — Security and Privacy

## The main risk

Connected-note systems often contain private pages, block references, attachments and relationship metadata. A publishing tool must prevent accidental disclosure, including disclosure through backlinks and embedded blocks.

## Safe-publication principles

- publish by explicit inclusion, not implicit exclusion;
- normalise into a separate public graph;
- fail the build when a public card references private embedded content;
- strip unsupported source metadata and local paths;
- keep credentials and provider tokens server-side;
- generate a manifest of every public route and asset;
- provide a dry-run report before publication.

## Responsible disclosure

Until a public repository and security contact are established, do not submit sensitive vulnerability details through a public issue. The future repository should publish a `SECURITY.md` with supported versions and a private reporting route.

## AI adapters

An AI adapter must be optional. It should use only the public corpus by default, cite sources, enforce limits and never expose a provider key to the browser.

