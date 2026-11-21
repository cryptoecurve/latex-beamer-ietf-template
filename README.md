# IETF-style Beamer template (4:3)

This is a reusable LaTeX Beamer recreation of the **uploaded PowerPoint** slide template.
It reproduces the original 4:3 slide ratio, dark teal title/header (`#002D3C`), off-white
body (`#FAFAFA`), text styling, standard Beamer-sized circular bullets, slide numbering, and the IETF logo supplied
in the PowerPoint (provided in two sizes).

## Files

- `beamerthemeIETFMinimal.sty`: Beamer visual theme.
- `example.tex`: five editable example slides matching the source deck.
- `ietf-logo-small.png`, `ietf-logo-title.png`: original logos extracted from the supplied PPTX.
- `example.pdf`: compiled preview.

## Compile

Install a LaTeX distribution with Beamer, TikZ, and fonts. LuaLaTeX is recommended
for the closest typography (Open Sans and Montserrat). Run:

```bash
lualatex example.tex
lualatex example.tex
```

If the fonts are unavailable, the theme uses available fallbacks. The presentation
uses a **4:3** Beamer aspect ratio (`aspectratio=43`). You can make slides in the usual way:

```tex
\begin{frame}{My slide title}
  \begin{itemize}
    \item Main point
    \begin{itemize}
      \item Supporting detail
    \end{itemize}
  \end{itemize}
\end{frame}
```

The first (title) frame should use `[plain]` and `\titlepage` so its white footer and
large logo are displayed instead of the normal slide number and small logo.

The slide numbers correspond to the reference file (the title slide is slide 1, even
though it does not display a number).
