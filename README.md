# Repolex Knowledge Graph of hashicorp/go-cleanhttp

RDF knowledge graph data for [hashicorp/go-cleanhttp](https://github.com/hashicorp/go-cleanhttp), parsed by [repolex](https://repolex.ai).

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
rlex download hashicorp/go-cleanhttp
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b0e8488e2fe29dce6a369099f264aa046c27b659
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b0e8488e2fe29dce6a369099f264aa046c27b659
│           └── chunk-001.nq.gz
├── blob
│   ├── 036e5313fc8f91fd38136ad16db65ef23ce69d64.nq.gz
│   ├── 0c6a85c24f644a2908becf11c7a11a7788f6e932.nq.gz
│   ├── 14d3f054f13e4f8e1335d8efc3cfd45185c6a221.nq.gz
│   ├── 4af220d0dcfd715fe6895315020231b79642d48a.nq.gz
│   ├── 4bdde03bb41448aad1d08057b1015757fcd4b1af.nq.gz
│   ├── 54103cb12a6d142a9e8bacd423cbc183992e85c7.nq.gz
│   ├── 5d29684d7aaf59e704217bea61fb79ebb7acd9d3.nq.gz
│   ├── 69c63bf9d1200203f417e2b551a06ecc84412036.nq.gz
│   ├── 6d1e382c20202c3d6455e9b7fdf30b2ae87f6620.nq.gz
│   ├── 72a13c9193edb7589b6a391ee2a739380f982f64.nq.gz
│   ├── 8b2b6740439447b47a157884c302937c61bb2cb7.nq.gz
│   ├── bfc77887d07f47102fc47f79f968eaeecf855629.nq.gz
│   ├── d3609b4ff95dbda3dcae7692d1ffe36360f21839.nq.gz
│   ├── ed73dac6a725ddd590eb0590b6c5364e2b7d3b34.nq.gz
│   └── fc99b73154d60c42f3df592ae51d0c8a4077167d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b0e8488e2fe29dce6a369099f264aa046c27b659.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
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

[hashicorp/go-cleanhttp](https://github.com/hashicorp/go-cleanhttp)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
