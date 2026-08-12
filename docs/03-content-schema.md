# 03 — Content Schema

This is a conceptual schema for public discussion. It is not yet a stable specification.

## Card example

```yaml
schema: puliweave/card/v0.1
id: idea-001
slug: connections-before-categories
status: published
visibility: public
theme: orange
title:
  en: Connections before categories
  zh-Hans: 连接先于分类
summary:
  en: "A short proposition."
  zh-Hans: "一段简短的命题。"
blocks:
  en:
    - id: idea-001-b01
      type: paragraph
      text: "One focused block of text."
relationships:
  - target: idea-002
    type: supports
    label:
      en: Provides an example
sources:
  - type: url
    href: https://example.org/source
    title: Example source
publication:
  owner: example-author
  reviewed_at: 2026-08-12
```

## Required properties

- `id`: permanent and unique;
- `slug`: route-friendly current name;
- `visibility`: explicit public/private boundary;
- `title`: at least one language;
- `blocks`: the card body;
- `relationships`: typed links to stable IDs;
- `publication`: ownership and review metadata.

## Relationship example

```yaml
- target: idea-002
  type: supports
  visibility: public
  label:
    en: Adds practical evidence
```

Suggested initial vocabulary:

- `relates_to`
- `supports`
- `challenges`
- `applies_to`
- `part_of`
- `cites`
- `derived_from`
- `demonstrated_by`
- `discussed_in`

## Wiki links and block references

A source adapter may recognise notations such as `[[Page Name]]` and block references, but the normalised record should resolve them to stable IDs. Display syntax must never be the only representation of a relationship.

## Multilingual behaviour

IDs and relationships are language-neutral. Titles, summaries, blocks, link labels, accessibility labels and metadata can vary by language. A build declares whether fallback to another language is permitted.

