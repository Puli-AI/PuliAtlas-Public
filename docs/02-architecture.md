# 02 — Public Architecture

## Proposed pipeline

```text
private notes or structured files
            ↓ explicit export policy
normaliser and schema validator
            ↓
public content graph
       ┌────┼─────────┐
       ↓    ↓         ↓
    index  graph     cards
       └────┼─────────┘
            ↓
static site artifact
            ↓
GitHub Pages / object storage / Nginx / other host
```

## Components

### Import adapters

Adapters convert supported sources into a neutral PuliWeave record. The first adapters should be:

1. native YAML/JSON;
2. Markdown with wiki links;
3. Roam Research JSON export.

### Normaliser

The normaliser creates stable node and block IDs, resolves page links, classifies relationships and rejects ambiguous or private material according to the publication policy.

### Validator

The validator reports:

- duplicate and missing IDs;
- broken links;
- links to excluded/private nodes;
- unknown relationship types;
- missing required text and accessibility labels;
- incomplete translation states;
- oversized or unsupported media.

### Static builder

The builder generates:

- stable HTML routes;
- language bundles;
- the graph dataset;
- search and backlink indexes;
- metadata, sitemap and feeds;
- a version and content manifest.

### Optional services

Comments, authentication, analytics and AI are adapters—not requirements for publishing. They should never be prerequisites for reading the public cards.

## Trust boundary

The builder must assume that the source graph may contain private notes. A safe implementation publishes only records explicitly marked public and then checks that no public record embeds excluded content through a block reference or attachment.

