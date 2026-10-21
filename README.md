# Repolex Knowledge Graph of executablebooks/python-pkg-cookiecutter

RDF knowledge graph data for [executablebooks/python-pkg-cookiecutter](https://github.com/executablebooks/python-pkg-cookiecutter), parsed by [repolex](https://repolex.ai).

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
rlex download executablebooks/python-pkg-cookiecutter
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e8ee7a8c517396496b04eb701d7462dc3f580a78
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e8ee7a8c517396496b04eb701d7462dc3f580a78
│           └── chunk-001.nq.gz
├── blob
│   ├── 0756306d0fd3c3eab2571bd6f8d3eb2c7eadd1a7.nq.gz
│   ├── 187d4ce4e5d1f11ea6f764a7f320b8ae44130923.nq.gz
│   ├── 262d89e064bc9c73129c89325c15bcdbc662ecc4.nq.gz
│   ├── 2bf2dbe5f58d665f0cd884452540477d80583275.nq.gz
│   ├── 3482a4f0e7a3dd739d75d734bb82d3dab9cce269.nq.gz
│   ├── 39baf331b8e968f2b1f685e5a0edc72c90b087de.nq.gz
│   ├── 527d9e2a04e092546fe33dd1ee657b4f507b0e01.nq.gz
│   ├── 56723b5523b8f88d9696e5bb6d1b55fa244af415.nq.gz
│   ├── 56739cebc25937b7760aefad7c95886ca29735ea.nq.gz
│   ├── 5f485e522fa78676f9777d570856901a56a81773.nq.gz
│   ├── 60f7395c50c0ada3178dfebdfffe352cb540c71f.nq.gz
│   ├── 65e7dd5154f986453fdddb64a081a946345fd95a.nq.gz
│   ├── 6966869c7054c18810eb323772b93ba5a42cefc5.nq.gz
│   ├── 6b1d0bfabc3c1cfa396e0270c55fdcec96919fba.nq.gz
│   ├── 6c0f1623fbdea360c92e5a273b57c0a28e20f464.nq.gz
│   ├── 789c9d06d6d0616120adfb52387b9ec9f203126b.nq.gz
│   ├── 7dbeaba8146d6b53088c6709aa317cb8f0fd95e5.nq.gz
│   ├── 81a191e7afec69f5af4c39e8646deadf41481706.nq.gz
│   ├── 851867571ce601ed1749b600f71d9ee2d29de452.nq.gz
│   ├── 8c2b54db853a56ef6c2de75e244ce4e304f71afa.nq.gz
│   ├── 914a4f5a233dede578264860912339428c96a3e1.nq.gz
│   ├── 935f817ead86643c60b8df9913d2d97355fd2f51.nq.gz
│   ├── 96a6fa5a1b9916332984076b3934577a411efbea.nq.gz
│   ├── 989f564d66bd5e3b304187202a5c56d7b34a227b.nq.gz
│   ├── 9e5815d528af7e9f70f26d0499bfe34a1a8cca1f.nq.gz
│   ├── a47dee7b50483305d8de35094454f298d20f2dc3.nq.gz
│   ├── acb867017e11bfa7c3bd4cb86fc82cc40733e97f.nq.gz
│   ├── c1dc0600afb08acff5f5db66ef983fa0d8619272.nq.gz
│   ├── cad6b098c84d7dcb140a937ea3ce7730ebdbf371.nq.gz
│   ├── cd0f23ba0a3a5786ce5c912f231d3097ca467645.nq.gz
│   ├── d05be2579c38c84b59c477335f733c3eea71c07a.nq.gz
│   ├── d5a973355fc34b6aa1358c0da1f5fe9b0f05d415.nq.gz
│   ├── db3e396a37896c3256e10def7103532e38586709.nq.gz
│   ├── ddfb6350900b24d5932351e2c283b2c22b216555.nq.gz
│   ├── dfe0770424b2a19faf507a501ebfc23be8f54e7b.nq.gz
│   ├── e079f8a6038dd2dc8512967540f96ee0de172067.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f118455f590c31dc8c2d742f22867b061ccfe736.nq.gz
│   └── fb76d2f75dd473ccfce3a5bf8d58740547ad9c93.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e8ee7a8c517396496b04eb701d7462dc3f580a78.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 45 files
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

[executablebooks/python-pkg-cookiecutter](https://github.com/executablebooks/python-pkg-cookiecutter)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
