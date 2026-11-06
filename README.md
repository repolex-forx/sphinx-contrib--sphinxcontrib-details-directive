# Repolex Knowledge Graph of sphinx-contrib/sphinxcontrib-details-directive

RDF knowledge graph data for [sphinx-contrib/sphinxcontrib-details-directive](https://github.com/sphinx-contrib/sphinxcontrib-details-directive), parsed by [repolex](https://repolex.ai).

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
rlex download sphinx-contrib/sphinxcontrib-details-directive
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── eaa929e41aebdad977ee43405259ac50d2aa0a10
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── eaa929e41aebdad977ee43405259ac50d2aa0a10
│           └── chunk-001.nq.gz
├── blob
│   ├── 04641b6865434ddf86233281e5cbb6169f71d939.nq.gz
│   ├── 17dbfa359a8c6932e72822965a804766faa63099.nq.gz
│   ├── 2961440d12abcddd05d9fadb45d9d62da9376582.nq.gz
│   ├── 2a71d07c58a9e4590cdec6e345d9f23ae1a2a215.nq.gz
│   ├── 3b70fa315f0e411ed15041759ee8761351856c99.nq.gz
│   ├── 4d65d7a4b5098ba23ebbfaac691c6f91c599a100.nq.gz
│   ├── 4fb7d7059cc9a4474825e61012ffae77022e6e95.nq.gz
│   ├── 6cdf1a5c5f40c294b0fb3f1b5162ec4f8b8d5a9f.nq.gz
│   ├── 8dede9817b3c86379ebc33176fc20fc836a540dc.nq.gz
│   ├── 9278a5b9804821b1fe1b73ef73d17e6480db6960.nq.gz
│   ├── ab5e68832a337dbb1722dbede381134affafe87a.nq.gz
│   ├── b6b9fd7a21c970765d25a8f5a1c1281eb9211aa5.nq.gz
│   ├── bc1d8e5bd24e9e93526d807f4cd2475ad27ebbd4.nq.gz
│   ├── bfdbe9ac05d69ac822cc31a082bef4a3b183e2e3.nq.gz
│   ├── cdcdbba304b71c44c7f672e6f1f0b7bf81c3d49d.nq.gz
│   └── dab9419bb0d3a43ad523fde210d3ac0fd0cbbecc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── eaa929e41aebdad977ee43405259ac50d2aa0a10.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 24 files
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

[sphinx-contrib/sphinxcontrib-details-directive](https://github.com/sphinx-contrib/sphinxcontrib-details-directive)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
