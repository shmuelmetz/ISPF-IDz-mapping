# ISPF-LPEX-mapping

Tables of Live Parsing Editor (LPEX) equivalents to ISPF/PDF EDIT primary
and line commands, parsed from the IBM reference manuals.

<!-- LPEX expansion: "Live Parsing Editor" per Clark (2003), as quoted in
     the Wikipedia LEXX article; AcronymFinder gives "Live Parsing
     Extensible Editor" instead -- the two disagree on the last word and
     the discrepancy is unresolved. -->

## Background

[ISPF/PDF EDIT](https://www.ibm.com/docs/en/SSLTBW_3.2.0/pdf/f54em00_v3r2.pdf)
and the
[LPEX editor](https://www.ibm.com/docs/en/developer-for-zos/latest?topic=editors-introduction-z-systems-lpex-editor)
share a common heritage: LPEX is a reimplemented derivative of
[LEXX](https://en.wikipedia.org/wiki/LEXX_(text_editor)), written by Mike
Cowlishaw of IBM in 1985 for VM/CMS. LPEX was originally produced for
OS/2 and AIX, and now also runs on Windows, Linux, and the Java JVM. The
two editors use different command names and syntax for many equivalent
operations. This project provides a systematic cross-reference derived
directly from the IBM documentation.

## Contents

- [`primary-commands.md`](primary-commands.md) — all 54 ISPF Edit primary
  commands, with LPEX equivalents where the LPEX documentation confirms one
- [`line-commands.md`](line-commands.md) — all 28 ISPF Edit line commands,
  with LPEX equivalents where confirmed
- `ISPF-LPEX-mapping.bib` — bibliography for the reference manuals used

## Sources

Links verified 2026-09-04.

| Key | Document |
|-----|----------|
| `IDzLPEX` | [Introduction to the z Systems LPEX Editor](https://www.ibm.com/docs/en/developer-for-zos/latest?topic=editors-introduction-z-systems-lpex-editor) |
| `LPEXCmd` | [z Systems LPEX commands](https://www.ibm.com/docs/en/developer-for-zos/latest?topic=editor-z-systems-lpex-commands) |
| `LPEXShortcuts` | [z Systems LPEX Editor keyboard shortcuts](https://www.ibm.com/docs/en/developer-for-zos/latest?topic=editors-z-systems-lpex-editor-keyboard-shortcuts) |
| `LPEXISPFCmds` | [ISPF commands supported in z Systems LPEX Editor](https://www.ibm.com/docs/en/developer-for-zos/latest?topic=commands-interactive-system-productivity-facility-lpex) |
| `LPEXISPFProfile` | [ISPF base profile](https://www.ibm.com/docs/en/developer-for-zos/latest?topic=profiles-ispf-base-profile) |
| `SC19362170` | [z/OS 3.2 ISPF Edit and Edit Macros (PDF, SC19-3621-70)](https://www.ibm.com/docs/en/SSLTBW_3.2.0/pdf/f54em00_v3r2.pdf) — primary and line command summaries at topics `commands-edit-primary-command-summary` and `commands-line-command-summary` |

## Status

Command tables complete for the commands each source documents. Not yet
done: LPEX's own native commands that have no ISPF counterpart at all
(out of scope for a table keyed by ISPF command), and a decision on
whether to chase down primary sources for the ISPF commands current LPEX
documentation doesn't mention (may simply be unsupported, may just be
undocumented on that one page — see the Notes column in each table).
