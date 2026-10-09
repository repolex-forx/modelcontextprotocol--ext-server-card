# Repolex Knowledge Graph of modelcontextprotocol/ext-server-card

RDF knowledge graph data for [modelcontextprotocol/ext-server-card](https://github.com/modelcontextprotocol/ext-server-card), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download modelcontextprotocol/ext-server-card
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 526201bbc80231daa40ffcdecfc9da4e54e5dc93
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 526201bbc80231daa40ffcdecfc9da4e54e5dc93
│           └── chunk-001.nq.gz
├── blob
│   ├── 20f168d0d02825a410565253da7ff9e58fc9de7a.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 3c4593898b1d436e8bae6bcf93d33dfdf968ea61.nq.gz
│   ├── 47dc3e3d863cfb5727b87d785d09abf9743c0a72.nq.gz
│   ├── 48299d744b2c2a3c0ca53b5890bacc704584b22f.nq.gz
│   ├── 53314cdf4cb0a09777a40e9115793e2dd5c91067.nq.gz
│   ├── 5f9d7c6c9fd2d4801f21a3652ef987574b4dbe3e.nq.gz
│   ├── 8269b209b39ce1972e2e1eedc6b018eed425a045.nq.gz
│   ├── 85872f9de68ba6bb1e5d3571ca298de6012aa22e.nq.gz
│   ├── 95493b642d91990977e8b3580c649398089e9ffa.nq.gz
│   ├── 9fda00273cf1f82d4cc7cc46be6ff6964d354179.nq.gz
│   ├── a09d8edc15ae3bc2f79fdefb3c4fabf32aa62148.nq.gz
│   ├── a93de9481e1a2456ad006003ff774a323ce91f55.nq.gz
│   ├── af7eb8cf2aa8d988ce6702b5da8f25b2382423f8.nq.gz
│   ├── b1f65207f2f1b1eb3d39a568500fe4ca2d75baa4.nq.gz
│   ├── bc4bdf78002d29f5789de01ee373ca26e215eceb.nq.gz
│   ├── c30bb1d909c9f821dba01ee97b86ed003a7ca8ee.nq.gz
│   ├── ce3f3bc5d4c1509de3faffde326590ec04184e85.nq.gz
│   ├── e4f822bfb1dd7e59edd3438c5b9703dc2214459b.nq.gz
│   ├── f04b8e91062e7dc36a7141ad7c68f42fc3cdf387.nq.gz
│   ├── f541b4757bd8f82f18c1996234306985bdeb2e1c.nq.gz
│   └── feb06fa29fc64b326da8f1677688516f05104cbe.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 526201bbc80231daa40ffcdecfc9da4e54e5dc93.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[modelcontextprotocol/ext-server-card](https://github.com/modelcontextprotocol/ext-server-card)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
