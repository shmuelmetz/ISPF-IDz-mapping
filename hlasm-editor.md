# ISPF Edit commands → IDz HLASM Editor equivalents

IBM Developer for z/OS (IDz) has a second, distinct editor for Assembler
besides LPEX: the Eclipse-native **HLASM Editor** (`HLASMEditor` in
[`ISPF-LPEX-mapping.bib`](ISPF-LPEX-mapping.bib)). Unlike LPEX, it has no
ISPF-profile personality at all — it's a standard Eclipse editor with
HLASM-specific enhancements layered on top, so its interaction model
(mouse, menus, and Eclipse's own keybindings) is fundamentally different
from ISPF's prefix-area/command-line model, not just a different set of
command names for the same model.

Because of that, most rows below map an ISPF *command* to a generic
Eclipse *keybinding* (`EclipseKeys` in the bib file, official Eclipse
Platform documentation) rather than to another discrete command — "press
Ctrl+C" is doing the job "enter C in the prefix area" did, but it isn't
itself a documented HLASM-specific feature. Blank means neither source
documents an equivalent; that's not proof one doesn't exist, only that
it isn't confirmed.

Links verified 2026-09-04.

## Primary commands

| ISPF command | HLASM Editor equivalent | Notes |
|---|---|---|
| CANCEL | | |
| CHANGE | Find/Replace dialog (`Ctrl+F`) | Generic Eclipse, not HLASM-specific |
| COPY | | |
| CUT | Cut (`Ctrl+X`) | ISPF CUT supports multiple named clipboards; Eclipse has one system clipboard |
| DELETE | `Delete` key on a selection | Generic Eclipse |
| EXCLUDE | | No documented fold/hide feature |
| FIND | Find/Replace dialog (`Ctrl+F`); also see Find References below | Ctrl+F is generic Eclipse; Find References is HLASM-specific |
| HILITE | Syntax highlighting | Always on; not a toggle the way ISPF's HILITE primary command is |
| LOCATE | Go to Line (`Ctrl+L`) | Generic Eclipse |
| MOVE | Cut (`Ctrl+X`) then Paste (`Ctrl+V`) | Generic Eclipse |
| PASTE | Paste (`Ctrl+V`) | Generic Eclipse |
| RFIND | Find Next (`Ctrl+K`) | Not identical: Ctrl+K repeats a search on the currently *selected* text, not literally "the last FIND command's string" |
| SAVE | Save (`Ctrl+S`) | Generic Eclipse |
| UNDO | Undo (`Ctrl+Z`) | Generic Eclipse |

All other ISPF primary commands (AUTOLIST, AUTONUM, AUTOSAVE, BOUNDS,
BROWSE, BUILTIN, CAPS, COMPARE, CREATE, DEFINE, EDIT, EDITSET, END,
FLIP, HEX, HIDE, IMACRO, LEVEL, MODEL, NONUMBER, NOTES, NULLS, NUMBER,
PACK, PRESERVE, PROFILE, RCHANGE, RECOVERY, RENUM, REPLACE, RESET,
RMACRO, SETUNDO, SORT, STATS, SUBMIT, TABS, UNNUMBER, VERSION, VIEW)
have no confirmed HLASM Editor equivalent.

## Line commands

| ISPF command | HLASM Editor equivalent | Notes |
|---|---|---|
| ( | Shift Left (`Shift+Tab`) | Shifts by one indent unit, not a specific character count the way ISPF's `(`*n* does |
| ) | Shift Right (`Tab`) | Same caveat as `(` |
| < | Shift Left (`Shift+Tab`) | Same caveat |
| > | Shift Right (`Tab`) | Same caveat |
| C, CC | Copy (`Ctrl+C`) on a selection | Generic Eclipse |
| D, DD | `Delete` on a selection | Generic Eclipse |
| I | Position cursor, press `Enter` | Not a discrete command, just ordinary text entry |
| M, MM | Cut (`Ctrl+X`) then Paste (`Ctrl+V`) | Generic Eclipse |

All other ISPF line commands (A/AK, B/BK, BOUNDS, COLS, F, L, LC/LCC,
MASK, MD, O/OK, R/RR, S, TABS, TE, TF, TS, UC/UCC, X/XX) have no
confirmed HLASM Editor equivalent — in particular, block-marking targets
(A/B/O) and exclude/duplicate/case-conversion line commands don't
correspond to any single documented Eclipse or HLASM Editor action.

## HLASM Editor features with no ISPF equivalent

These aren't gaps in this cross-reference — ISPF Edit genuinely has
nothing like them, because it treats HLASM source as plain text with no
language awareness at all:

- **Content Assist** (`Ctrl+Space`) — suggests instructions, symbols, and
  macros (default `SYS1.MACLIB`, current-file, and local custom macros)
- **Find References** — locates and highlights other occurrences of the
  selected language element
- **Open Declaration** — jumps to the definition of a symbol, copy
  member, or macro
- **Hover Help** — shows information for symbols, instructions, and
  macros on mouseover
- **Outline View** — structural navigation by macro, CSECT, DSECT,
  RSECT, COM, LOCTR, branch target, and symbol name
- **Real-time syntax checking** — validates HLASM syntax as you type

ISPF's own `L` (label) and `T` (tag) line commands are the closest thing
it has to structural navigation, but they're plain editor bookmarks with
no relationship to HLASM syntax — unlike the Outline View above, which
is genuinely structural. LPEX makes the same distinction for the same
reason: it parses HLASM structurally (outline tree, optional COPY
expansion) where ISPF just sees text.
