# Repolex Knowledge Graph of UKPLab/emnlp2026-claim-flow

RDF knowledge graph data for [UKPLab/emnlp2026-claim-flow](https://github.com/UKPLab/emnlp2026-claim-flow), parsed by [repolex](https://repolex.ai).

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
rlex download UKPLab/emnlp2026-claim-flow
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 181e5778e0a350ba41b3b643ec747c517b95d90f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 181e5778e0a350ba41b3b643ec747c517b95d90f
│           └── chunk-001.nq.gz
├── blob
│   ├── 041749946831e9e8f862fde6206fa943e43a73b5.nq.gz
│   ├── 24ee5b1be9961e38a503c8e764b7385dbb6ba124.nq.gz
│   ├── 278e92b5335dfa009a1c5c52ee301bf6039ebab3.nq.gz
│   ├── 2a9b51fddf714ca547f6d69744eb95ab542f5d4f.nq.gz
│   ├── 2bf181be99efc231af377631a1fbb4434aeff355.nq.gz
│   ├── 33dc20faa2912d6b26fc0bd44c2c54de76a45534.nq.gz
│   ├── 46a259cba7ec763326f28ef800486a8ac61aab1f.nq.gz
│   ├── 491ebd1adaad2b8e41f052ffa07391798f6278d1.nq.gz
│   ├── 4ac8c03a4d171f0c4da0f9e0b156abc964c830f3.nq.gz
│   ├── 72ba94aa0728728a1151bd21484304cab9227a50.nq.gz
│   ├── 784e3459f83e993a4a546aab1eeed4daf95ce660.nq.gz
│   ├── 84694aab8ff4585febd21be70db934d9a3014beb.nq.gz
│   ├── a18d3935960609f6933f6fcfa0d8960b614e9236.nq.gz
│   ├── ab88cb13e1969738accd74581ffb1e0de9e2f593.nq.gz
│   ├── b4ca98421cb93c1ba38868ff4b53959cbe593af8.nq.gz
│   ├── c43d9a63dfb9c304dc75e0dcc1c160e72e8e9496.nq.gz
│   ├── c9ce68ab4c11c8b2f8b01500961bea9793bf5647.nq.gz
│   ├── dee5599ccf7520ed9b36129aa31c99330003d7de.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 181e5778e0a350ba41b3b643ec747c517b95d90f.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 26 files
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

[UKPLab/emnlp2026-claim-flow](https://github.com/UKPLab/emnlp2026-claim-flow)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
