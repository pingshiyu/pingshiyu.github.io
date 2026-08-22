# Curriculum vitae

The folder contains two CV variants:

- `main.tex` is the full academic CV.
- `industry.tex` is tailored to industry research scientist and research
  engineer applications.

Both are adaptations of Subidit's
[Star Rover](https://github.com/subidit/rover-resume/tree/main/templates/star%20rover)
template. See `TEMPLATE-LICENSE.md` for attribution and licensing.

Build it with:

```sh
latexmk -pdf main.tex
latexmk -pdf industry.tex
```

or, if `latexmk` is unavailable:

```sh
pdflatex main.tex
pdflatex main.tex
pdflatex industry.tex
pdflatex industry.tex
```

This adaptation uses LaTeX's built-in sans-serif font and plain-text contact
labels instead of Star Rover's optional Fira Sans and Font Awesome packages. On
Debian or Ubuntu, the remaining packages are provided by:

```sh
sudo apt install texlive-latex-extra
```

Alternatively, upload the folder to Overleaf and compile there with pdfLaTeX.