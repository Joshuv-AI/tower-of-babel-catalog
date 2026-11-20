# Tower of Babel — Catalog

The **Tower of Babel** is a free digital library operated by [Antarctic Labs](https://antarctic-labs.com).
It holds **2,557,923 public-domain and rights-clear texts**, every one with full text and metadata.
No accounts, no paywalls.

**Library:** https://antarctic-labs.com/tower-of-babel

This repository is the library's catalog record for developers, researchers, and harvesters:
what the collections are, how big they are, and how to pull the catalog into your own system.
The catalog summary also lives here as machine-readable JSON: [`catalog-summary.json`](catalog-summary.json).

## Collections

| Collection | Records | OAI set |
|---|---:|---|
| Law (US law) | 1,277,197 | `law` |
| Papers (scholarly papers) | 1,130,210 | `papers` |
| Books | 81,631 | `books` |
| Reference | 41,137 | `reference` |
| Declassified documents | 26,294 | `declassified` |
| Podcasts (transcripts) | 1,091 | `podcasts` |
| Documents | 363 | `documents` |
| **Total** | **2,557,923** | |

Counts are from the 2026-11-16 catalog snapshot; the library grows daily.

## Harvest the catalog (OAI-PMH)

The library exposes a standard OAI-PMH 2.0 endpoint in `oai_dc` and `oai_openaire` formats:

```
https://antarctic-labs.com/oai
```

Examples:

```
# Identify the repository
https://antarctic-labs.com/oai?verb=Identify

# List the collections (sets)
https://antarctic-labs.com/oai?verb=ListSets

# Harvest one collection, e.g. Books
https://antarctic-labs.com/oai?verb=ListRecords&metadataPrefix=oai_dc&set=books
```

Each record carries title, author, year, a link to the work's page in the library,
a link to the full text, and a rights statement. Every work is public domain or
otherwise rights-clear. Podcast records are metadata-only in the feed.

One operational note: all records share a single snapshot datestamp (2026-11-16),
because the catalog carries no per-entry dates. Harvest `ListRecords` in full
rather than relying on incremental from/until harvesting.

## Other access

- **Web library:** https://antarctic-labs.com/tower-of-babel
- **API access:** https://antarctic-labs.com/tower-of-babel/library/research
- **Per-work pages:** every record's OAI `identifier` links resolve to the work's page on the site.

## About

The Tower of Babel is a preservation library: public-domain books, sacred texts,
declassified documents, scholarly papers, law, and transcripts, kept in clean,
searchable text. It is run by Antarctic Labs, an independent laboratory, and was
founded in 2026.

Contact via the site: https://antarctic-labs.com/contact
