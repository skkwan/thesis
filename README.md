# Thesis 

See `main.tex` and `main.pdf`.

## Nifty things

- [To-Do highlight extension](https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight) 
- `aspell`:
  ```bash
  aspell check -l en *.tex  
  ```
- If a citation is added with incorrect formatting to the `.bib`, the auto-rebuild will throw errors and refuse to fix itself. In this case, delete the `main.pdf`, and the re-build should show the citations again.
- [Git LaTeXdiff](https://gitlab.com/git-latexdiff/git-latexdiff)
  To install, in a separate directory:
  ```bash
  git clone https://gitlab.com/git-latexdiff/git-latexdiff.git
  make install 
  # "make install" failed for me, so I used the suggested command which installs without the man page
  /Library/Developer/CommandLineTools/usr/bin/make install-bin
  ```
  Then to call it, back in the thesis top-level directory:
  ```bash
  git latexdiff HEAD~1 --main main.tex
  ```