# Repolex Knowledge Graph of python-trio/sniffio

RDF knowledge graph data for [python-trio/sniffio](https://github.com/python-trio/sniffio), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download python-trio/sniffio
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cb8a03d45371efb20156ec895003a9bd988ac89b
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── cb8a03d45371efb20156ec895003a9bd988ac89b.nq.gz
│   └── repolex
│       └── cb8a03d45371efb20156ec895003a9bd988ac89b
│           └── chunk-001.nq.gz
├── blob
│   ├── 104c402ebf17ef55f9cdca2114f0a4449f6dd039.nq.gz
│   ├── 133b89f554a3ae181dc07bf5dbd9b69cc316b48a.nq.gz
│   ├── 291bfeaa3b207e4173c50080f22cfb473363ee5a.nq.gz
│   ├── 2a62cea5a0a34136b4ab8c84089f616ac0654883.nq.gz
│   ├── 2c71c9d662a8386fb39cb4c7d1bd35c67ea1275e.nq.gz
│   ├── 374839c052ead785f987357d5cf7f94f4e4c7126.nq.gz
│   ├── 47ad4b1d6f68df976d9c63307c411ebab7daa205.nq.gz
│   ├── 4cd8acfcac6fac8c3f21168ab5280a585394697d.nq.gz
│   ├── 4edd4b18b3f9a2893c3d0a37e5e747a5f09cebe7.nq.gz
│   ├── 518b8c375d090ddda558aa282ee2b8e4d6e334f1.nq.gz
│   ├── 51f3442917839f8e0f0cccb52b3c10968ad0779e.nq.gz
│   ├── 5a5f906bbf9194d624facc763022721a96a4a3b4.nq.gz
│   ├── 6414b3ebfcba20aad33ddd706e18afff7c38a838.nq.gz
│   ├── 6742196cb2535493adbb7941ab0a279c0f39b0e2.nq.gz
│   ├── 67898ba6f5cffa770a3110d8c996c8203cbbdc26.nq.gz
│   ├── 6d45a38edcd4b10c2e73f352e4cf90167f4423a0.nq.gz
│   ├── 7370e0e146230e7c0d935bc13f9c1abb95cd9662.nq.gz
│   ├── 76a28299ab326f25fe6d4285c018d51a3127236d.nq.gz
│   ├── 7fb30ff405a3e087b0ccaa1f554d048933b72591.nq.gz
│   ├── 93227db00343f029d1b56e3b5056502b34fdc498.nq.gz
│   ├── 938a98f24314376f217d36f45f4c8e9c17a63235.nq.gz
│   ├── 984c8c00d148e6d3915dc65e122c8380c7adb562.nq.gz
│   ├── b8bb97185926d7daed314609753173945ed4ff1a.nq.gz
│   ├── bab85fc38f4d8df1b588c82343b4e705f2657b9b.nq.gz
│   ├── c1a7bbf218ba985b87cd1d9b23da69222894c1dd.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── da6abdf2ce977fc22ed876f6b16a95a7fa4341da.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f38c5167733eb2fd1cb677450f876788a4aa603e.nq.gz
│   └── fb3364d7f1f8d16b49c1a86dce73b478c54d5f89.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── cb8a03d45371efb20156ec895003a9bd988ac89b.nq.gz
├── filetree
│   └── cb8a03d45371efb20156ec895003a9bd988ac89b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 40 files
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

## Source repository

[python-trio/sniffio](https://github.com/python-trio/sniffio)

---
*Parsed on 2026-04-09 by [repolex](https://repolex.ai)*
