# Curriculum vitae

The download landing page is served at `/cv/` via `index.html`. It is intentionally
not linked from the homepage. The folder contains three CV variants:

- `main.tex` is the full academic CV.
- `main-zh.tex` is its Simplified Chinese translation, with publication titles
  and author names retained in English for citation. Keep its content and dates
  in sync with `main.tex`.
- `industry.tex` is tailored to industry research scientist and research
  engineer applications.

All are adaptations of Subidit's
[Star Rover](https://github.com/subidit/rover-resume/tree/main/templates/star%20rover)
template. See `TEMPLATE-LICENSE.md` for attribution and licensing.

Build the English PDFs with:

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

The English variants use LaTeX's built-in sans-serif font and plain-text contact
labels instead of Star Rover's optional Fira Sans and Font Awesome packages. On
Debian or Ubuntu, the remaining packages are provided by:

```sh
sudo apt install texlive-latex-extra
```

Build the Chinese PDF with XeLaTeX (pdfLaTeX does not support this source):

```sh
latexmk -xelatex main-zh.tex
```

or:

```sh
xelatex main-zh.tex
xelatex main-zh.tex
```

The Chinese variant uses `xeCJK`, Latin Modern Sans, and Noto Sans CJK SC. Noto
includes the character 洴 in the author's name, which the standard Fandol fonts
omit. On Debian or Ubuntu, install the additional packages:

```sh
sudo apt install texlive-xetex texlive-lang-chinese fonts-noto-cjk
```

Alternatively, upload the folder to Overleaf and compile the English variants
with pdfLaTeX and `main-zh.tex` with XeLaTeX.

Commit the generated PDFs alongside their sources so all three landing-page
downloads work on GitHub Pages; no server-side build is required.
