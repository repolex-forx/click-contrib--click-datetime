# Repolex Knowledge Graph of click-contrib/click-datetime

RDF knowledge graph data for [click-contrib/click-datetime](https://github.com/click-contrib/click-datetime), parsed by [repolex](https://repolex.ai).

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
rlex download click-contrib/click-datetime
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 942964cf71b5c43a542e63e634c934ab29d3daf3
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 942964cf71b5c43a542e63e634c934ab29d3daf3
│           └── chunk-001.nq.gz
├── blob
│   ├── 24378bc067712b565eac24ae8fd6eb2f60395971.nq.gz
│   ├── 2b186578044115bd08a70b1fee0c62952d8398b7.nq.gz
│   ├── 34cd5243c3b32fd4ce2ada04027723e3c966340c.nq.gz
│   ├── 376b77ae8f44a06787d5910191c713c986791a72.nq.gz
│   ├── 3f69cad53cb0c392d2963c25445da4a5c05d8ee3.nq.gz
│   ├── 557b4a050d24902bacb2af6a2d07d0174118a60e.nq.gz
│   ├── 62a77e59c9dd1c895bc0d2c7124230c21f086120.nq.gz
│   ├── 7f908d9686c40ac4574eca977071e413bd88bdf1.nq.gz
│   ├── a6f442aa225d0249cc584586ecaaad297ddb8cb4.nq.gz
│   ├── c26bf6a3d561818801b8a54ede89ca7e3e0587fa.nq.gz
│   ├── e342cace9094f0cfba2ede471378144760e55b27.nq.gz
│   └── f9582f0245552287ed8a5041b42140f50db375fd.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 942964cf71b5c43a542e63e634c934ab29d3daf3.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 20 files
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

[click-contrib/click-datetime](https://github.com/click-contrib/click-datetime)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
