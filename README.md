# Repolex Knowledge Graph of aio-libs/aiomcache

RDF knowledge graph data for [aio-libs/aiomcache](https://github.com/aio-libs/aiomcache), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aiomcache
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── bf912d16f4a3e7c81b1680b49c39a42d18ab0d91
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── bf912d16f4a3e7c81b1680b49c39a42d18ab0d91
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ab77a06f3eb8a8137293aa4e2f16ca889a2e546.nq.gz
│   ├── 1a66886859f377fee65003a623b8e41fde388dd0.nq.gz
│   ├── 1b5506c3efc30150bee16fe37b76f60562239616.nq.gz
│   ├── 27a92fa8a356594a5b9f4d7a5bf5afb1e887beb2.nq.gz
│   ├── 36979982708b367032730848375b2a457cf360b8.nq.gz
│   ├── 39ae898eeb0b425a69b2b356dfe097e7a8ba9dc2.nq.gz
│   ├── 3ea39a8c7aa9650bab50869dba6c6b6b62552a41.nq.gz
│   ├── 4a0ff2b8af6dcd7f07a74c74afc296cbba915c2e.nq.gz
│   ├── 55a1e26699561817c8125f1e40ec977f841eb44b.nq.gz
│   ├── 6ab07d11df1265d96acb964bc56c637bd493ee27.nq.gz
│   ├── 6e2a7cc499ab0fa6f258d2b33b3ffcc4362e6fa5.nq.gz
│   ├── 75256c16e7318bf807c0699a6d055ebf07750457.nq.gz
│   ├── 79f3bc3b7d337711c46ca432aa88587f6662d2e8.nq.gz
│   ├── 7b702612803a76f998cd12592942d8f7d456de1a.nq.gz
│   ├── 9696c440e4667bb67f56fa647e0a3b67037b7e63.nq.gz
│   ├── a2e2138534b908daa5567af478d205794592bfdb.nq.gz
│   ├── aa40d7e25a7b5514e20df68fc2ad049ba494bed9.nq.gz
│   ├── ac74b7941b9d619457c425ed00a7600ebc25b2d6.nq.gz
│   ├── aee4b6856869584d3f1d9150c523444177e28a70.nq.gz
│   ├── b5762bd9d2277e90f67579b7a014ee6e5d2d4f15.nq.gz
│   ├── b9fb8a6e0f4a5ce99899eb97d872c6b90f4bb678.nq.gz
│   ├── bd9baabfd9707ba8bf0c28e00b69674f1ebf586a.nq.gz
│   ├── bea058c6fb47c31e9729c26d128b5bff81a08aa1.nq.gz
│   ├── cc0f9553a31e4edab4f3edea0945f3f0408e72c3.nq.gz
│   ├── d2f87363f0bd29aab47fcca0ff5913bcd1db6873.nq.gz
│   ├── d41d23f629a522c3af54180ad6bf216a6b112e3f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e7a2daf20999a843dd43f347e2533e14d8a2effe.nq.gz
│   ├── ec3a64f7352d95f7e2c60c3177c9b5e1ed0611f7.nq.gz
│   ├── ed5965f8e0dad5b1fc997e1d762308f80df42a99.nq.gz
│   ├── f46c5417855cd7819be9f330ab50f77e80d43586.nq.gz
│   └── f8a115dcb38be7c367834c977414917077ef37dc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── bf912d16f4a3e7c81b1680b49c39a42d18ab0d91.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[aio-libs/aiomcache](https://github.com/aio-libs/aiomcache)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
