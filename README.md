# Repolex Knowledge Graph of asimov-modules/asimov-ftp-module

RDF knowledge graph data for [asimov-modules/asimov-ftp-module](https://github.com/asimov-modules/asimov-ftp-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-ftp-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 871afead6d72567c1a43807679994e89ecba6c6c
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 871afead6d72567c1a43807679994e89ecba6c6c.nq.gz
│   └── repolex
│       └── 871afead6d72567c1a43807679994e89ecba6c6c
│           └── chunk-001.nq.gz
├── blob
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 17e51c385ea382d4f2ef124b7032c1604845622d.nq.gz
│   ├── 2258cfc513af6c77c94b9f61c61ca14767497cb0.nq.gz
│   ├── 291d5c37438bc9aca527999054f61fdab89078dc.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 740a85e4bc9868eb68733f3c9d6ef5178a259479.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 8bcfa2698147dd6f559522cae1f1d044e690fda7.nq.gz
│   ├── 9693e6fdb760270b98e0957d442184840f74c4ca.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── a78e6ade792ef8aeab8b5e5935d4b4d4fbfa5a94.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── c152b6f4a32a1d318e7145d52ad63678d76ffefb.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── ee4d9362508d63f9e156fe9ee1b11ebc1a3e86d6.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 871afead6d72567c1a43807679994e89ecba6c6c.nq.gz
├── filetree
│   └── 871afead6d72567c1a43807679994e89ecba6c6c.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 27 files
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

[asimov-modules/asimov-ftp-module](https://github.com/asimov-modules/asimov-ftp-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
