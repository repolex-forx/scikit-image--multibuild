# Repolex Knowledge Graph of scikit-image/multibuild

RDF knowledge graph data for [scikit-image/multibuild](https://github.com/scikit-image/multibuild), parsed by [repolex](https://repolex.ai).

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
rlex download scikit-image/multibuild
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0623c582027a5c914a24d5e0823d5e3c47d43101
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0623c582027a5c914a24d5e0823d5e3c47d43101
│           └── chunk-001.nq.gz
├── blob
│   ├── 15eae6b3c2951b5e6067f9ab42f46971c66ea742.nq.gz
│   ├── 1f401e527d16b2024e5ede467e4bf47dbaf161f9.nq.gz
│   ├── 278564ea0ce7b49d791396cf58917a0d55eb780b.nq.gz
│   ├── 2908a9b5b80ae166635b39f734b09e13bf59f343.nq.gz
│   ├── 31f0704d47dbacc20cf8fe27bfe596c864ded58d.nq.gz
│   ├── 349ea14e2b95ee338ac24f9989f660d60353884e.nq.gz
│   ├── 3c259ac9a0e1cf1273b14e30cbdf7cef35ecb4c8.nq.gz
│   ├── 47779d72adcf7e18e11bb417553e8a74d88d5cf9.nq.gz
│   ├── 4995f4117efbb366bde313f10fe9d22647f12e7f.nq.gz
│   ├── 588e1bdc096eb29b89daf13197e3224c5d81a51c.nq.gz
│   ├── 5da61647cc010b0d677b914fa0a18dc619f5b6f3.nq.gz
│   ├── 69138638d9e8597694841e71b1e012d3986bacf6.nq.gz
│   ├── 740c5e61441f030282393afda263559eebb0967a.nq.gz
│   ├── 77bc91c9bd36863a54a4109b6ddc5cd9141039ab.nq.gz
│   ├── 79cba33c1fb92140df4aaa12295281fc2c4613af.nq.gz
│   ├── 87b0f3537854af383668862679cc0af21994befb.nq.gz
│   ├── 941e4ff2a2f64de9eb97097af0a60a4d33677545.nq.gz
│   ├── 9afc1229ee2f06e279a64dd4f1b954f52ef16801.nq.gz
│   ├── 9be9f40877b30f901d468024217003531c95bc6c.nq.gz
│   ├── a29579d3dd87c62cedbe88aceb7925810c3acebe.nq.gz
│   ├── a33ac02041b42510453ced1064b45bd5efc86713.nq.gz
│   ├── a3cf9ed851ac5e6904c728b4b4301234c58ac5f7.nq.gz
│   ├── b2d3133b40372244712fb703a45fef4654272964.nq.gz
│   ├── bd82fad135f36a40632da7fb7958103bfe6d403f.nq.gz
│   ├── c9daa5032a4c3d1baaa706248264417673e27a5e.nq.gz
│   ├── de8cccb98e930767f000f3ca982e1721584d009f.nq.gz
│   ├── e47e9034c4116f467618cfaaa4d3aca004094007.nq.gz
│   ├── f226337e08b5319b86b3f28e118af176f7abaded.nq.gz
│   ├── f2483271682a4270d40a2dde3f7814bc0fe9e97b.nq.gz
│   └── f75c04289fd798655d609de3aa524342af0464d9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0623c582027a5c914a24d5e0823d5e3c47d43101.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 36 files
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

[scikit-image/multibuild](https://github.com/scikit-image/multibuild)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
