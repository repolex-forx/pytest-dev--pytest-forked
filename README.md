# Repolex Knowledge Graph of pytest-dev/pytest-forked

RDF knowledge graph data for [pytest-dev/pytest-forked](https://github.com/pytest-dev/pytest-forked), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-forked
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0126c65af046c7a231e2415ac2f373706d5f8517
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0126c65af046c7a231e2415ac2f373706d5f8517
│           └── chunk-001.nq.gz
├── blob
│   ├── 276091c2e87d51ca64b56f4d229ea2f7726a7995.nq.gz
│   ├── 3d67a9c864c1d7a2a130eb4742366dfba3b3869d.nq.gz
│   ├── 4e540b8d429159c01f8034aa9b12d2a85d10489c.nq.gz
│   ├── 58d06e3cdd2c16b972ab28347005c8a0ab959477.nq.gz
│   ├── 67c99d66e5f9089f14cdf88c419fcb3cb167ef5d.nq.gz
│   ├── 6d135cb7c2b0fc9822914b00b0095baf726533ca.nq.gz
│   ├── 8daa234cd53898421952b237467d366ec3dfe0c0.nq.gz
│   ├── a4263f4119aec3db562963a6e11e679367084611.nq.gz
│   ├── b4327125feb77a205a2125ed297e81e4b5b4d40d.nq.gz
│   ├── bed56b4405cfbb3d38fa1d279f87d529c9e93ad3.nq.gz
│   ├── d6fa0282f9728e462ef712e579f3c0b137fdb17b.nq.gz
│   ├── e43687f3240b3a864ab978a1147979528994a355.nq.gz
│   ├── ec884a8bc0fca3d535f9b85f9987859d3188899a.nq.gz
│   ├── f4726f29bcf7afacb05e9e51389ccc5d93ad3d11.nq.gz
│   ├── fe6e527c9a729e92b237eca9f5553c45e4611bdc.nq.gz
│   └── ff33b8f7ca0b1c05bb0bdc546aa760c8e78757be.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0126c65af046c7a231e2415ac2f373706d5f8517.nq.gz
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

[pytest-dev/pytest-forked](https://github.com/pytest-dev/pytest-forked)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
