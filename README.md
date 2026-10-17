# Repolex Knowledge Graph of jplana/python-etcd

RDF knowledge graph data for [jplana/python-etcd](https://github.com/jplana/python-etcd), parsed by [repolex](https://repolex.ai).

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
rlex download jplana/python-etcd
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d2889f7b23feee8797657b19c404f0d4034dd03c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d2889f7b23feee8797657b19c404f0d4034dd03c
│           └── chunk-001.nq.gz
├── blob
│   ├── 1059eef12097f70766cec621b3382541bb663bab.nq.gz
│   ├── 11d9138c8069f1ab4b2105f9043e585897d779dc.nq.gz
│   ├── 131e81d091ec726db0a7a0a442b69d921018c2b8.nq.gz
│   ├── 2f790dd7268cff54076f9e66ba7153dce90259a0.nq.gz
│   ├── 31f5086689fedfdca0c9953220f93e78c5e67f6a.nq.gz
│   ├── 372f10c3432d17bb5bed6c1433c65925439c3a95.nq.gz
│   ├── 37cdee1778ec861b326ce36dc47798fa7dc38db4.nq.gz
│   ├── 39f8db71ee8dfb72f05b65ec71e25d6afce8c5b5.nq.gz
│   ├── 5996872e003c9ce492f6676bfc134cefdc8474cf.nq.gz
│   ├── 631a14b6f176648708d26f90ba108a403d1593b2.nq.gz
│   ├── 716c8835169a8a6785e8fd94a802a3e130280fe1.nq.gz
│   ├── 7685dcaf74891ad98ee6e42cd5e18fe23ccdd5a5.nq.gz
│   ├── 8b94a705b0f69064e32560cfeeaf0ce3f219f4f8.nq.gz
│   ├── 8bbc4d339bec4f16766ee758dd82719b05787dd1.nq.gz
│   ├── 8d68c00a057e120d895186fc14323f8402504bdc.nq.gz
│   ├── 9814b86bb4cf7c1e1e61b62ac6cdc7fd2a3976c7.nq.gz
│   ├── a01175741fcfab6e23b2c799f45978d4cfdf029f.nq.gz
│   ├── a1930681b61eccd6458f1dad885008a44cb79a3c.nq.gz
│   ├── a1b95c4437e2d6d50d4c74883c28587717b4fcfd.nq.gz
│   ├── b660c24dbe1032f29ad85721074d707757757762.nq.gz
│   ├── c8b441151fcb4cd9f82971b8ff14c1d256964a68.nq.gz
│   ├── ce1b0c973fd6ebc673d255a78115c5f90667e36d.nq.gz
│   ├── d716e9bec041b1a60a74342d51c791728aaea665.nq.gz
│   ├── d782d163831084c2b53255608e793e66c29ddfe4.nq.gz
│   ├── e34a526c5931fe18317de23250a094d160f8aaad.nq.gz
│   ├── e35d68575fdc8ba952e8eacc4b1410d2fc39734e.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ee8141fc3bfde4101e03d980aadb5c9541aae507.nq.gz
│   ├── f122882fd25091d25c9f2b05aa48d24cfad8f73f.nq.gz
│   └── f9e97dd43e02aa80fd64c9182df97142e008bf9c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d2889f7b23feee8797657b19c404f0d4034dd03c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 38 files
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

[jplana/python-etcd](https://github.com/jplana/python-etcd)

---
*Parsed on 2026-10-17 by [repolex](https://repolex.ai)*
