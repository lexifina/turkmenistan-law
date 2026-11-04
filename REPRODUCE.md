# How this repository was made (Turkmenistan)

This file is written by the build on 2026-11-04, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| Türkmenistanyň Mejlisi (mejlis.gov.tm): Kanunçylyk | <https://mejlis.gov.tm/laws?lang=tm> | 2026-10-28 | Official text; site "Ähli hukuklar goralan" |
| Mejlis of Turkmenistan: official laws and codes | <https://mejlis.gov.tm/laws?lang=tm> | 2026-11-04 | Official legislative documents excluded from copyright under Law 257-IV, Article 7. |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `konstitusiya` | Türkmenistanyň Konstitusiýasy | 1 | 2023-01-21 to 2023-01-21 |
| `rayat-kodeksi` | Türkmenistanyň Raýat kodeksi | 1 | 2026-01-01 to 2026-01-01 |
| `mejlis-law-384` | Türkmenistanda ahalteke bedew atlarynyň döwlet goragy hakynda | 1 | 2026-09-23 to 2026-09-23 |
| `mejlis-law-378` | Wirtual aktiwler hakynda | 1 | 2026-01-01 to 2026-01-01 |
| `mejlis-law-047` | Psihologik hyzmatlar hakynda | 1 | 2020-01-01 to 2020-01-01 |
| `mejlis-law-058` | Durmuş-zähmet gatnaşyklaryny düzgünleşdirmek boýunça üçtaraplaýyn topar hakynda | 1 | 2019-01-01 to 2019-01-01 |
| `mejlis-law-125` | Neşe serişdeleri, psihotrop maddalar, prekursorlar we olaryň bikanun dolanyşygyna garşy hereket etmek hakynda | 1 | 2018-01-01 to 2018-01-01 |
| `mejlis-law-078` | Türkmenistanyň çägini operatiw enjamlaşdyrmak hakynda | 1 | 2018-01-01 to 2018-01-01 |
| `mejlis-law-081` | Ganyň donorlygy hakynda | 1 | 2018-01-01 to 2018-01-01 |
| `mejlis-law-066` | Şahsy durmuş barada maglumat we ony goramak hakynda | 1 | 2017-07-01 to 2017-07-01 |
| `mejlis-law-122` | Türkmenistanyň Söwda-senagat edarasy hakynda | 1 | 2016-01-01 to 2016-01-01 |
| `mejlis-law-123` | Ekstremizme garşy hereket etmek hakynda | 1 | 2015-07-01 to 2015-07-01 |

The build made 12 commits:

| Commits | Kind |
| ---: | --- |
| 12 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-11-04.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 2 laws in the record.
- 13 tags.

## Dates

Each commit is dated at noon (Asia/Ashgabat) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: A law enters into force on the day its own text names; Turkmen laws state it in their final article ("… kabul edilen pursadyndan güýje girýär", "… herekete girizilýär"). https://mejlis.gov.tm/single-law/107?lang=tm

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `20a40125a655f6c456cb9e281ae838d411887aae77b8bafeff8c5cd99dbeddd2` (1265466 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `35388bee5aa05369f7da68f5a8fa015ea8d442b8`, `check.py` `5d719354ea4c62d240c93d2cae446307d81d9e81`, `on.py` `aff48cf1b68d50c7ba8f399ca32261871c301824`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

Not yet run for this build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- Constitution: "61" read as 6 superscript 1.
- Constitution: articles shown in the consolidated text only as a red "repealed by …" note are left out of the text: art-075.
- Criminal Code left out of this build: parser stopped (duplicate article art-070).
- mejlis-law-384: In-force basis: Signature/adoption date in official closing block; Şu Kanun gol çekilen pursadyndan herekete girizilýär.
- mejlis-law-378: In-force basis: Explicit commencement clause: Şu Kanun 2026 -njy ýylyň 1 -nji ýanwaryndan herekete girizilýär.
- mejlis-law-047: In-force basis: Explicit commencement clause: Şu Kanun 2020-nji ýylyň 1-nji ýanwaryndan herekete girizilýär.
- mejlis-law-058: In-force basis: Explicit commencement clause: Şu Kanun 2019-njy ýylyň 1-nji ýanwaryndan herekete girizilýär.
- mejlis-law-125: In-force basis: Explicit commencement clause: 1. Şu Kanun 2018-nji ýylyň 1-nji ýanwaryndan herekete girizilýär.
- mejlis-law-078: In-force basis: Explicit commencement clause: Şu Kanun 2018-nji ýylyň 1-nji ýanwaryndan güýje girýär.
- mejlis-law-081: In-force basis: Explicit commencement clause: 1. Şu Kanun 2018-nji ýylyň 1-nji ýanwaryndan güýje girýär.
- mejlis-law-066: In-force basis: Explicit commencement clause: 1. Şu Kanun 2017-nji ýylyň 1-nji iýulyndan güýje girýär.
- mejlis-law-122: In-force basis: Explicit commencement clause: 2. Şu Kanunyň V baby 2016-njy ýylyň 1-nji ýanwaryndan güýje girýär. The initial commencement was 2015-07-01; Chapter V commenced 2016-01-01. This single current-text record starts when both phases were operative.
- mejlis-law-123: In-force basis: Explicit commencement clause: Şu Kanun 2015-nji ýylyň 1-nji iýulyndan güýje girýär.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- Claude Code (Claude Opus 5.5, claude-opus-5-5) wrote Lexifina's code and chose the sources. No model wrote or altered legal text; all text is parsed by code from the official pages.
- GPT-6 wrote extraction and verification code. The six consolidated codes with unverified amendment commencement dates are held. No model wrote or corrected legal text.
