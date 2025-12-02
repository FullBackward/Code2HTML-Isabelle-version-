# Code2HTML-Isabelle-version-

This is an unofficial fix to the Code2HTML plugin used in JEdit, for Isabelle.
Fixes:
- Used package xcolor instead of color.
- Abandoned the old package \\usepackage[latin1]{inputenc} for encoding special characters from Isabelle; instead, used a combination of \\setmainfont{Latin Modern Roman}, \\setmathfont{Latin Modern Math}, and \\setmonofont{JetBrains Mono} to display special characters. Accordingly, the compiler uses XeLaTeX instead of pdfLaTeX.
- Fixed the indentation problem from the old version.
- In GenericDocument.Java there was a repeated call to the style constructors, resulting in a repeated style definition export in the LaTeX script generated. This was fixed by adding a style detection method.