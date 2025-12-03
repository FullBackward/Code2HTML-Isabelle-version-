# Code2HTML-Isabelle-version-

This is an unofficial fix to the Code2HTML plugin used in JEdit, for Isabelle.
Fixes:
- Used package xcolor instead of color.
- Abandoned the old package \\usepackage[latin1]{inputenc} for encoding special characters from Isabelle; instead, used a combination of \\setmainfont{Latin Modern Roman}, \\setmathfont{Latin Modern Math}, and \\setmonofont{JetBrains Mono} to display special characters. Accordingly, the compiler uses XeLaTeX instead of pdfLaTeX.
- Fixed the indentation problem from the old version.
- In GenericDocument.Java there was a repeated call to the style constructors, resulting in a repeated style definition export in the LaTeX script generated. This was fixed by adding a style detection method.

Note: local building requires local jedit.jar and docbook-xsl-1.49

## Installation for Isabelle2025 application

Since this is an unofficial fix, installation involves replacing the Code2HTML JAR file in JEdit.
1. Ensure Code2HTML is already present in the plugin list. If not, you can download it via the plugin manager. This should be installed by default when Isabelle2025 is installed.
   ![Screenshot 2025-12-03 at 10 52 52](https://github.com/user-attachments/assets/6ea9fabc-493d-4df8-afd9-16db28b6cc8c)

2. Navigate to Isabelle2025/contrib/jedit-20250215/jedit5.7.0-patched/jars, replace the original Code2HTML JAR file with your own compiled fixed Code2HTML JAR file or the compiled Code2HTML JAR file in the repo (make sure the name is Code2HTML.jar).

3. Restart Isabelle2025 to load the plugin. In the plugin manager, you should now see in the Author information, a new bracket that says: (updated by Xuanwei Ren).
   ![Screenshot 2025-12-03 at 11 00 03](https://github.com/user-attachments/assets/094b50a1-3454-41f4-abc9-ef65d082d994)
