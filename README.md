# Turkmenistan: law history in git

The law of Turkmenistan as a git history: one file per provision, one commit per version of an act on the day it took effect, and the law that made it as the commit's author. `git log` lists the versions of a provision; picking a date gives the text in force that day.

It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law), which places it at `tm/`. The texts are in Turkmen, the official language of the Mejlis texts.

**What is in it now**

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `konstitusiya/` | Türkmenistanyň Konstitusiýasy (the Constitution) | 1 | The Mejlis consolidated text: the 2016 revision as amended by the constitutional laws of 2017, 2020 and 2023 (No. 531-VI of 21 January 2023 is the latest) |
| `rayat-kodeksi/` | Türkmenistanyň Raýat kodeksi (the Civil Code) | 1 | As enacted by Kanun No. 162-VII of 28 June 2025, in force 1 January 2026 |

This is a first build, not a full history. Each act has one version, "the oldest version available": the Mejlis publishes only the current text, with no earlier versions online. The Constitution is dated 21 January 2023, the date of the latest amending law, which is assumed to be its in-force day; the in-force clause of No. 531-VI itself has not been checked. Article 75 of the Constitution appears in the source only as a "repealed" note and is left out. Article numbers with a superscript (such as 6 with a superscript 1) are written with a hyphen. The Criminal Code (revised edition, Kanun No. 456-VI of 17 April 2022) is not yet included.

## Dates

Each commit is dated at noon, Asia/Ashgabat, on the day the version took effect. Trailers on every commit name the law and the source; the in-force day is in `In-force:`.

## How it is checked

- The texts were fetched from the Mejlis a second time and parsed again; both runs give identical provisions.
- Every version is read back from git and compared with `corpus.json` (`tools/check_repo.py`); results are in `REPRODUCE.md`.
- No merge commits, no commit dates going backwards or in the future, and every commit's trailers parse with `git interpret-trailers --parse`.

## What "author" means

The author of a commit is the law that made the change, with an e-mail address that cannot exist, so `git blame` and `git log --author` name it. The committer is always Lexifina.

## Licence

See `LICENSE`. Laws are not objects of copyright in Turkmenistan (Law on Copyright and Related Rights, Article 7).
