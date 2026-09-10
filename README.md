# KJO Documentation

Technical documentation for the KJO Liquid Rocket Motor Control System.

## Document Suite

| Document | File | Description |
|---|---|---|
| System Overview | `System_Overview/KJO_System_Overview.tex` | Architecture, propellant flow, control flow, command set |
| RCU Reference | `RCU/KJO_RCU_Reference.tex` | Remote Control Unit hardware, software, and GUI |
| EMU Reference | `EMU/KJO_EMU_Reference.tex` | Engine Management Unit hardware, software, and valve control |
| GSEMU Reference | `GSEMU/KJO_GSEMU_Reference.tex` | GSE Management Unit hardware, software, and Fill valve |
| LCMU Reference | `LCMU/KJO_LCMU_Reference.tex` | Load Cell Management Unit hardware, software, CAN bus, and load cells |

## Repository Structure

```
KJO_Documentation/
├── shared/
│   ├── KJO_preamble.tex     ← Shared LaTeX packages, colors, macros
│   └── KJO_tikz_styles.tex  ← Shared TikZ node and line styles
├── System_Overview/
│   ├── KJO_System_Overview.tex
│   └── fig/
│       ├── propellant_flow.tex     ← Propellant system P&ID-style schematic
│       └── control_architecture.tex← Electronic control block diagram
├── RCU/
│   ├── KJO_RCU_Reference.tex
│   └── fig/
├── EMU/
│   ├── KJO_EMU_Reference.tex
│   └── fig/
├── GSEMU/
│   ├── KJO_GSEMU_Reference.tex
│   └── fig/
└── LCMU/
    └── KJO_LCMU_Reference.tex
```

## Compiling

Open any `.tex` file in TeXworks and compile with **pdfLaTeX**.
MiKTeX will auto-install any missing packages on first compile.

Each document is standalone and self-contained.
The `shared/` files are referenced via relative `\input` paths.

Compiled PDFs **are** committed to this repository alongside their `.tex`
sources, so the document suite is readable without a local LaTeX install.

## Version History

| Version | Date | Notes |
|---|---|---|
| 0.1 | March 2026 | Initial release — all four documents, complete first draft |
| 0.2 | September 2026 | Added LCMU Reference (fifth document). Fixed tables overflowing the page margin in all documents (`tabularx`/`Y` columns added to the shared preamble). Updated System Overview's architecture description and diagram for the CAN bus (EMU/GSEMU/LCMU) that replaced the old EMU–GSEMU GPIO handshake, and added LCMU throughout. Fixed a pre-existing TikZ error in the propellant-flow diagram (a node using `\\` without `align=`) that was silently corrupting that figure on every compile. |
