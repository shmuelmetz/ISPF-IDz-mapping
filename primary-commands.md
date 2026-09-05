# ISPF Edit primary commands → LPEX equivalents

Left column is the complete "Edit primary command summary" from the z/OS
ISPF Edit and Edit Macros manual (`SC19362170` in
[`ISPF-IDz-mapping.bib`](ISPF-IDz-mapping.bib)). Right column is drawn
from the z Systems LPEX Editor's ISPF-commands page (`LPEXISPFCmds` in
the same bib file), which documents only the commands it explicitly lists —
IBM's own text there says the ISPF profile "supports most, but not all,
commands available in ISPF." A blank LPEX column means the source page
doesn't document that command as supported, not that it's confirmed
absent.

Links verified 2026-09-04.

| ISPF command | LPEX equivalent | Notes |
|---|---|---|
| AUTOLIST | | |
| AUTONUM | | |
| AUTOSAVE | | |
| BOUNDS (BNDS) | `BOUNDS` (`BNDS`) | LPEX: column numbers only, no label range |
| BROWSE | | |
| BUILTIN | | |
| CANCEL | | |
| CAPS | | |
| CHANGE | `C` | Parameters: FIRST/LAST/NEXT/PREV/ALL, CHARS/WORD/SUFFIX/PREFIX, column numbers or label range; LPEX highlights only the current match instance, ISPF highlights all |
| COMPARE | | |
| COPY | | |
| CREATE | | |
| CUT | | |
| DEFINE | | |
| DELETE (DEL) | `DELETE` (`DEL`) | Parameters: ALL/X/NX/label range |
| EDIT | | |
| EDITSET | | |
| END | | |
| EXCLUDE | `X` | Parameters: FIRST/LAST/NEXT/PREV/ALL, CHARS/WORD/SUFFIX/PREFIX, column numbers or label range |
| FIND | `F` | Same parameter set as CHANGE; hex specification not accepted in LPEX |
| FLIP | `FLIP` | Inverts include/exclude status of each line |
| HEX | | |
| HIDE | | |
| HILITE | | |
| IMACRO | | |
| LEVEL | | |
| LOCATE | | |
| MODEL | | |
| MOVE | | |
| NONUMBER | | |
| NOTES | | |
| NULLS | | |
| NUMBER | | |
| PACK | | |
| PASTE | | |
| PRESERVE | | |
| PROFILE | | |
| RCHANGE | `RCHANGE` | Repeats the last CHANGE/`C` |
| RECOVERY | | |
| RENUM | | |
| REPLACE | | |
| RESET (RES) | `RESET` (`RES`) | Parameters: X/CHG/FIND |
| RFIND | `RFIND` | Repeats the last FIND/`F` |
| RMACRO | | |
| SAVE | | |
| SETUNDO | | |
| SORT | `SORT` | Parameters: A/D (ascending/descending), X/NX, column numbers or label range |
| STATS | | |
| SUBMIT | | |
| TABS | | |
| UNDO | | |
| UNNUMBER | | |
| VERSION | | |
| VIEW | | |
