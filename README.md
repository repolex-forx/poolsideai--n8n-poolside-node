# Repolex Knowledge Graph of poolsideai/n8n-poolside-node

RDF knowledge graph data for [poolsideai/n8n-poolside-node](https://github.com/poolsideai/n8n-poolside-node), parsed by [repolex](https://repolex.ai).

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
rlex download poolsideai/n8n-poolside-node
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f8e2b8201bfbcfcbb007788ac0dcdb688e3177e2
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── f8e2b8201bfbcfcbb007788ac0dcdb688e3177e2.nq.gz
│   └── repolex
│       └── f8e2b8201bfbcfcbb007788ac0dcdb688e3177e2
│           └── chunk-001.nq.gz
├── blob
│   ├── 01639eee19b4c3b3ae1e2fd567ca15644b35b6db.nq.gz
│   ├── 2bd25b6ceff022f3dac545507e4aa2b2e4a7efea.nq.gz
│   ├── 380b6d7f1451e8273593184fb0c1c7d6f87c91da.nq.gz
│   ├── 394b493442604a6d826bbc38fa2f11b63b9be3f5.nq.gz
│   ├── 4e98d97497b361ab942ee58e0fc2e99737b53470.nq.gz
│   ├── 6836451734e94a74c6d1b84ad462c9c1512fb1e2.nq.gz
│   ├── a69bdc1bbb21683fbaa989012f2cfcb7b29e4876.nq.gz
│   ├── a903ff1025547c62fdc85e4cbdf911f51e4596b0.nq.gz
│   ├── a9254750a71e8769a1836111346bc2015913974b.nq.gz
│   ├── ade19b656508e475c398014097529fb23094e64a.nq.gz
│   ├── caf35d25769fae65370bd37a63c952eb72b1abaf.nq.gz
│   ├── d80d5a1c7d04008bcf9eb320385555e9d5303274.nq.gz
│   ├── ee2842aa1740f201c4fbf5cb9f83f711e2159083.nq.gz
│   └── f6aab196863b9f791c10698a4459e8db2b3e3587.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── f8e2b8201bfbcfcbb007788ac0dcdb688e3177e2.nq.gz
├── filetree
│   └── f8e2b8201bfbcfcbb007788ac0dcdb688e3177e2.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 23 files
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

[poolsideai/n8n-poolside-node](https://github.com/poolsideai/n8n-poolside-node)

---
*Parsed on 2026-10-01 by [repolex](https://repolex.ai)*
