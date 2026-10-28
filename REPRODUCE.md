# How this repository was made (Turkmenistan)

This file is written by the build on 2026-10-28, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| Türkmenistanyň Mejlisi (mejlis.gov.tm): Kanunçylyk | <https://mejlis.gov.tm/laws?lang=tm> | 2026-10-28 | Official text; site "Ähli hukuklar goralan" |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `konstitusiya` | Türkmenistanyň Konstitusiýasy | 1 | 2023-01-21 to 2023-01-21 |
| `rayat-kodeksi` | Türkmenistanyň Raýat kodeksi | 1 | 2026-01-01 to 2026-01-01 |

The build made 2 commits:

| Commits | Kind |
| ---: | --- |
| 2 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-28.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 2 laws in the record.
- 3 tags.

## Dates

Each commit is dated at noon (Asia/Ashgabat) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: A law enters into force on the day its own text names; Turkmen laws state it in their final article ("… kabul edilen pursadyndan güýje girýär", "… herekete girizilýär"). https://mejlis.gov.tm/single-law/107?lang=tm

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `fadec9157b3281c3665a58c5845b2720110527c84dc4c163e317a9a5e9a7d3ee` (916696 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a4faa25af85facb64b956b372f6b528aafdd7ec1`, `check.py` `3e59cb6f05eccb94a9ec14431a7f6781221e83ef`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

Not yet run for this build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- Constitution: "61" read as 6 superscript 1.
- Constitution: articles shown in the consolidated text only as a red "repealed by …" note are left out of the text: art-075.
- Criminal Code left out of this build: parser stopped (duplicate article art-070).

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- Claude Code (Claude Opus 5.5, claude-opus-5-5) wrote Lexifina's code and chose the sources. No model wrote or altered legal text; all text is parsed by code from the official pages.
