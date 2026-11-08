# Repolex Knowledge Graph of langchain-ai/new-langgraph-project

RDF knowledge graph data for [langchain-ai/new-langgraph-project](https://github.com/langchain-ai/new-langgraph-project), parsed by [repolex](https://repolex.ai).

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
rlex download langchain-ai/new-langgraph-project
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6d3f42296052c74ce57f9615da2ede10ba8dbe7d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6d3f42296052c74ce57f9615da2ede10ba8dbe7d
│           └── chunk-001.nq.gz
├── blob
│   ├── 26262e498a875964db44a835d2db5b2fb3bf8ba3.nq.gz
│   ├── 2a493994fca89882c6ec196f1b655b1f192d0834.nq.gz
│   ├── 4bfd87862d0acd73748b2093c2c379a10e076b75.nq.gz
│   ├── 4e931d0b6db86db9f26077c0a4bce3c375e4ec08.nq.gz
│   ├── 57d0481d4b50c89fee2cb9e88242639d8e674028.nq.gz
│   ├── 5bd2dd24a19f19c1f7c3d9e7f39279b72a81c934.nq.gz
│   ├── 68169be7cf71fcf8852c6876893a336a6c175799.nq.gz
│   ├── 743c2a0fea526d63910fe7e3ffbb05cff7973839.nq.gz
│   ├── 9ccba2b20f1cc9d38aa8f60aa7d934c7d7176846.nq.gz
│   ├── ad7b68b0b8b66a4a18d59647f824c0be5018f2ec.nq.gz
│   ├── b8c38d48abab3144f713e695e355d6cd90da9eaf.nq.gz
│   ├── c7d5f47d64da8cf1776734a27aa2bf1c65a94f9b.nq.gz
│   ├── cd3bd38392ff20d4b023024d6fb2b1cfc886c9c1.nq.gz
│   ├── d02981b813d1e326717873a241e8c2c1c96859d0.nq.gz
│   ├── e06f9e38f4d177b0787cfe7118d2a05ed6f76255.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec66fc0ada00340287e2aa6dc6f56f12a64d2724.nq.gz
│   └── f2900f275c77d938f4c6644e314e4d84fece36d9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6d3f42296052c74ce57f9615da2ede10ba8dbe7d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[langchain-ai/new-langgraph-project](https://github.com/langchain-ai/new-langgraph-project)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
