# PuliAtlas

- **Status:** Public concept and documentation preview
- **Documentation version:** 0.2
- **Date:** 2026-09-04

This public repository is the documentation foundation for PuliAtlas. It does not publish the private hosted-service code, Puli Consulting’s private knowledge graph, client material, or production secrets.

PuliAtlas is a proposed publishing system for turning connected notes into a coherent, interactive website: a navigable index, a living graph and one focused card at a time.

It grew from Puli Consulting’s work on a graph-centred company website. The public project is intended to help writers, researchers, educators and organisations publish connected knowledge without exposing their private source workspace.

## The core experience

```text
numbered or curated index  ↔  interactive graph  ↔  focused note/card
```

- The index provides editorial entry points.
- The graph reveals relationships rather than replacing navigation.
- The card makes one idea readable within one page or viewport.
- A structured source keeps every representation consistent.

## Intended inputs

PuliAtlas may eventually accept:

- Roam Research exports;
- Markdown with wiki links;
- YAML or JSON following the public PuliAtlas schema;
- other graph-note systems through adapters.

No compatibility is implied until an importer is implemented and tested.

## Intended outputs

- a fast static website;
- interactive graph data;
- accessible cards with stable URLs and backlinks;
- bilingual or multilingual content bundles;
- deployable artifacts that do not contain private notes.

## Repository boundary

This public package contains product documentation and generic examples only. Private application code, tenant architecture, deployment controls, Puli Consulting’s private cards, credentials, and client material belong in the private `Puli-AI/PuliAtlas` repository or their separately governed systems.

## Documentation

- [Product principles](docs/01-product-principles.md)
- [Public architecture](docs/02-architecture.md)
- [Content schema](docs/03-content-schema.md)
- [Roadmap](docs/04-roadmap.md)
- [Credits and acknowledgements](docs/05-credits.md)
- [Security and privacy](docs/06-security-and-privacy.md)
- [Contribution guide](CONTRIBUTING.md)

## Naming and licensing

**PuliAtlas** is the approved product name for this connected-knowledge publishing product. It is one product within Puli Consulting’s broader **myPuli** family; myPuli is not limited to PuliAtlas.

The project was called **PuliWeave** during its initial documentation phase. The repository was renamed on 2026-09-04, preserving that history. Trademark, domain and package-name clearance remain pending.

Publication on GitHub does not itself grant an open-source licence. Until Puli Consulting selects and adds a formal licence, the documentation and any future code should be treated as all rights reserved. See [LICENSE-NOTICE.md](LICENSE-NOTICE.md).
