# KJO Documentation

Technical documentation for the KJO Liquid Rocket Motor Control System.

## Document Suite

| Document | File | Description |
|---|---|---|
| System Overview | `System_Overview/KJO_System_Overview.tex` | Architecture, propellant flow, control flow, command set |
| RCU Reference | `RCU/KJO_RCU_Reference.tex` | Remote Control Unit hardware, software, and GUI |
| EMU Reference | `EMU/KJO_EMU_Reference.tex` | Engine Management Unit hardware, software, and valve control |
| GSEMU Reference | `GSEMU/KJO_GSEMU_Reference.tex` | GSE Management Unit hardware, software, and Fill valve |

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
└── GSEMU/
    ├── KJO_GSEMU_Reference.tex
    └── fig/
```

## Compiling

Open any `.tex` file in TeXworks and compile with **pdfLaTeX**.
MiKTeX will auto-install any missing packages on first compile.

Each document is standalone and self-contained.
The `shared/` files are referenced via relative `\input` paths.

PDFs are **not** committed to this repository — compile locally.

## Version History

| Version | Date | Notes |
|---|---|---|
| 0.1 | March 2026 | Initial release — all four documents, complete first draft |
