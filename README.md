# ISPF-LPEX-mapping

Tables of IBM Developer for z/OS (IDz) editor equivalents to ISPF/PDF
EDIT primary and line commands, parsed from the IBM reference manuals.
IDz has two distinct editors for mainframe source, and this project
covers both: the **LPEX** editor (which optionally emulates an ISPF
personality) and the Eclipse-native **HLASM Editor** (which doesn't).

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

IDz's [HLASM Editor](https://www.ibm.com/docs/en/developer-for-zos/latest?topic=files-hlasm-editor)
is a separate component with no shared heritage or code with LPEX — it's
a standard Eclipse editor with Assembler-specific enhancements (content
assist, an outline view, real-time syntax checking) layered on top, and
it has no ISPF-profile personality at all. Because its interaction model
is Eclipse's own menus and keybindings rather than ISPF's prefix-area
commands, its mapping table looks different from the LPEX ones — see
[`hlasm-editor.md`](hlasm-editor.md) for the details.

## Contents

- [`primary-commands.md`](primary-commands.md) — all 54 ISPF Edit primary
  commands, with LPEX equivalents where the LPEX documentation confirms one
- [`line-commands.md`](line-commands.md) — all 28 ISPF Edit line commands,
  with LPEX equivalents where confirmed
- [`hlasm-editor.md`](hlasm-editor.md) — the same ISPF commands mapped to
  IDz's Eclipse-native HLASM Editor instead of LPEX
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
| `HLASMEditor` | [IDz HLASM Editor](https://www.ibm.com/docs/en/developer-for-zos/latest?topic=files-hlasm-editor) |
| `EclipseKeys` | [Eclipse Platform: List of Key Bindings](https://help.eclipse.org/latest/topic/org.eclipse.platform.doc.user/reference/ref-keybindings.htm) |
| `SC19362170` | [z/OS 3.2 ISPF Edit and Edit Macros (PDF, SC19-3621-70)](https://www.ibm.com/docs/en/SSLTBW_3.2.0/pdf/f54em00_v3r2.pdf) — primary and line command summaries at topics `commands-edit-primary-command-summary` and `commands-line-command-summary` |

## Status

Command tables complete for the commands each source documents. Not yet
done: LPEX's own native commands that have no ISPF counterpart at all
(out of scope for a table keyed by ISPF command), and a decision on
whether to chase down primary sources for the ISPF commands current LPEX
or HLASM Editor documentation doesn't mention (may simply be
unsupported, may just be undocumented on that one page — see the Notes
column in each table).
