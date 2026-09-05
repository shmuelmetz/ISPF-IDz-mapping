# ISPF Edit line commands → LPEX equivalents

Left column is the complete "Line command summary" from the z/OS ISPF
Edit and Edit Macros manual (`SC19362170` in
[`ISPF-IDz-mapping.bib`](ISPF-IDz-mapping.bib)). Right column is drawn
from the z Systems LPEX Editor's ISPF base profile page (`LPEXISPFProfile`
in the same bib file), which states these prefix commands "function as
standard ISPF equivalents with no noted differences." A blank LPEX
column means the source page doesn't document that command as
supported, not that it's confirmed absent — IBM's own text says the
ISPF profile "supports most, but not all, commands available in ISPF."

Links verified 2026-09-04.

| ISPF command | LPEX equivalent | Notes |
|---|---|---|
| ( | `(` / `((` | Shift left one or *n* characters; `((` shifts a marked block |
| ) | `)` / `))` | Shift right one or *n* characters; `))` shifts a marked block |
| < | `<` / `<<` | Shift left with space validation; `<<` for a marked block |
| > | `>` / `>>` | Shift right with truncation protection; `>>` for a marked block |
| A, AK | `A` | Insert-after target for a copy/move; LPEX doesn't document a separate AK form |
| B, BK | `B` | Insert-before target for a copy/move; LPEX doesn't document a separate BK form |
| BOUNDS | | Not documented on the LPEX ISPF-profile page (LPEX does support a `BOUNDS`/`BNDS` *primary* command — see [primary-commands.md](primary-commands.md) — but not this line command) |
| C | `C` / `CC` | Copy one line or a marked block |
| COLS | | |
| D | `D` / `DD` | Delete one line or a marked block |
| F | `F` | Display first line(s) of an excluded block |
| I | `I` | Insert one or more blank lines |
| L | `L` | Display last line(s) of an excluded block |
| LC | `LC` / `LCC` | Convert to lowercase, one line or a marked block |
| M | `M` / `MM` | Move one line or a marked block |
| MASK | | |
| MD | | |
| O, OK | `O` / `OO` | Overlay target for a copy/move; LPEX doesn't document a separate OK form |
| R | `R` / `RR` | Repeat one line or a marked block |
| S | | |
| TABS | | |
| TE | | |
| TF | | |
| TS | | |
| UC | `UC` / `UCC` | Convert to uppercase, one line or a marked block |
| X | `X` / `XX` | Exclude one line or a marked block |

`/` (enter in the prefix area to make that line current) is documented
on the LPEX ISPF-profile page as supported, but doesn't appear as its
own row in the ISPF manual's Line command summary table above — it's
covered separately in ISPF's own documentation as a cursor-positioning
convention rather than a line command with an edit action.
