# Repolex Knowledge Graph of AlinaSchan/gasweek

RDF knowledge graph data for [AlinaSchan/gasweek](https://github.com/AlinaSchan/gasweek), parsed by [repolex](https://repolex.ai).

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
rlex download AlinaSchan/gasweek
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── deb2d217d7cba07fbfb7f7507b90ce62fe36e737
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── deb2d217d7cba07fbfb7f7507b90ce62fe36e737.nq.gz
│   └── repolex
│       └── deb2d217d7cba07fbfb7f7507b90ce62fe36e737
│           └── chunk-001.nq.gz
├── blob
│   ├── 042464dc9b99375cc7e4c3c662a8a2b585e30b87.nq.gz
│   ├── 0633232bfd99675631ebeabc00c168108311298c.nq.gz
│   ├── 0aeefc2bdbdd1570d91573b0daae2ae7701342c4.nq.gz
│   ├── 0ef17d892c10d347e004095e576266ad693ef5fd.nq.gz
│   ├── 106b76299d4db9a9f8ff337b898157f44cbe79d3.nq.gz
│   ├── 11a4389f3c246c48de11631ba4e1892fed09f612.nq.gz
│   ├── 1757a3dc8b49e06e1dd67d5fa2b51105672c4e07.nq.gz
│   ├── 2bd6118dbe3615a2284673c308feae0e54f48b9b.nq.gz
│   ├── 2d3a86a857e94e5a46fe4939dcb7a2f1813db9f6.nq.gz
│   ├── 3be38dc2f181982ff9ddece548c5498977f88bc3.nq.gz
│   ├── 54940d589943cdd5cba14b437a3ff4808cf9909d.nq.gz
│   ├── 554807664a3ce11a9b6d3a63c0d5bd01f3a8b21d.nq.gz
│   ├── 57ef6544cc2791de7237eb9f79fffb08d156080e.nq.gz
│   ├── 629785e9917ba6d5291154aaa4469e632f2c1685.nq.gz
│   ├── 76750e647c749e2a0f259cfe4d0fb79bc8637222.nq.gz
│   ├── 81c29dc6b8a3af27f37980ae6e494b272812993d.nq.gz
│   ├── 839c66244a050a4141d7f43f3969442d6db48b4d.nq.gz
│   ├── 98781a2a39174d2a5eba6600cb81fffcc0ddf4f8.nq.gz
│   ├── a4edb914c2285639daea0341870c7e302ad9432e.nq.gz
│   ├── a62c248e1ffa5507a023c47196d87e8b4854f2c5.nq.gz
│   ├── bfaa65f1d5386440942b79b6a33ef0470f2f1881.nq.gz
│   ├── c184d5b15de830529292b825c2f96d5e0255280d.nq.gz
│   ├── c1cb0fca4f1e2ac343b2126481f573a82c02969d.nq.gz
│   ├── c30c62e6f3a5f846c6e9f3fc83b987371442cdb3.nq.gz
│   ├── d999cae37f8eeddfae0e8aa8a7ea390751308cf5.nq.gz
│   ├── dc9f418ca619c5e2b9922d5d3b9e3f5bd9888067.nq.gz
│   ├── dd8a8c90e6b7af74ed3657ef5b74aaa5ebf0abd4.nq.gz
│   ├── efe3f6a5e17fde4c025eed5c024d02465a997eb6.nq.gz
│   └── f382081d4ab826ca21c0007da4ed951977b55ba1.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── deb2d217d7cba07fbfb7f7507b90ce62fe36e737.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 37 files
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

[AlinaSchan/gasweek](https://github.com/AlinaSchan/gasweek)

---
*Parsed on 2026-09-24 by [repolex](https://repolex.ai)*
