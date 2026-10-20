# Repolex Knowledge Graph of asottile/set-delete-branch-on-merge

RDF knowledge graph data for [asottile/set-delete-branch-on-merge](https://github.com/asottile/set-delete-branch-on-merge), parsed by [repolex](https://repolex.ai).

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
rlex download asottile/set-delete-branch-on-merge
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d8a1163e8febd4d3961f06e2ebefb32afefd3773
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d8a1163e8febd4d3961f06e2ebefb32afefd3773
│           └── chunk-001.nq.gz
├── blob
│   ├── 08a80902981665d69335b5b6ffdc116344373e37.nq.gz
│   ├── 175415dc58571fc1ce28d08678d7bb340b34cc57.nq.gz
│   ├── 8004f108284b1dcd1c3f5446e36063b3cf64c66b.nq.gz
│   ├── f1543fad215851e7e301b045b4b8f95a1e446d9c.nq.gz
│   └── fc4996c45a6a6851e99c025cad0ea08c9e88bc35.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d8a1163e8febd4d3961f06e2ebefb32afefd3773.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 12 files
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

[asottile/set-delete-branch-on-merge](https://github.com/asottile/set-delete-branch-on-merge)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
