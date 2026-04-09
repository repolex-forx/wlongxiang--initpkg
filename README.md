# Repolex Knowledge Graph of wlongxiang/initpkg

RDF knowledge graph data for [wlongxiang/initpkg](https://github.com/wlongxiang/initpkg), parsed by [repolex](https://repolex.ai).

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
lexq download wlongxiang/initpkg
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9521da8da5286b62fad6f3266f1da03009b1d2f0
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 9521da8da5286b62fad6f3266f1da03009b1d2f0.nq.gz
│   └── repolex
│       └── 9521da8da5286b62fad6f3266f1da03009b1d2f0
│           └── chunk-001.nq.gz
├── blob
│   ├── 1276d0254ffc2b5e4fcf48cd868123238d4ad06f.nq.gz
│   ├── 224a77957f5db48dfa25c8bb4a35f535202da203.nq.gz
│   ├── 298ea9e213e8c4c11f0431077510d4e325733c65.nq.gz
│   ├── 59ba092bf71e860afe55c9dcb6166af14f5d5d31.nq.gz
│   ├── 5eebc633566127bb7fa0470a32866607f4e40826.nq.gz
│   ├── 62ac892e3514816ff2020ebdf6aea0ad707e11f4.nq.gz
│   ├── 6e52361a698499c1a4b9499c02814ba37d455d7e.nq.gz
│   ├── 7893348a1b7dbb588983a48e6991282eae7e1b55.nq.gz
│   ├── 809e05ebf0a698689437c6612f22c10d345c3db0.nq.gz
│   ├── 82bfbed8ee55af69bd1cca9a7b107b5513d10873.nq.gz
│   ├── 8bdb800aaff6d2cc83697536ba308392f131741a.nq.gz
│   ├── 9346f9262ccbafacaf9dd0d387cd21041570767e.nq.gz
│   ├── aae46c90322a6cc8a3ec689e897cc4ec76253d0d.nq.gz
│   ├── b3c06d488393abb3b3829e5590d42409c995b4cf.nq.gz
│   ├── bc7b66f071fba1a8ff059fe73e5e769fcdc573c5.nq.gz
│   ├── c17f58bd8607971bab696c404b985dd6ca0c9561.nq.gz
│   ├── c1d71f7d998ec5618fdeccd7b3e414c03a50c2c6.nq.gz
│   ├── ce6b82303f6f5b9fe71658a5d0f6614e6186d179.nq.gz
│   ├── d4230bb515a1829874718fb294a5e6f816be39e4.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e9714c08fac09ce6c0e7dfd86fad3ec4d5b34823.nq.gz
│   ├── ea3be475cd733b0ec128dc74bd456d98cb05e06e.nq.gz
│   └── ef7a0889aa11163f74cb6446aa10c9c456e11d82.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 9521da8da5286b62fad6f3266f1da03009b1d2f0.nq.gz
├── filetree
│   └── 9521da8da5286b62fad6f3266f1da03009b1d2f0.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[wlongxiang/initpkg](https://github.com/wlongxiang/initpkg)

---
*Parsed on 2026-04-09 by [repolex](https://repolex.ai)*
