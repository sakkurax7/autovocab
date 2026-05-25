# autovocab

A LaTeX package for automatically collecting and linking vocabulary words in lecture notes.

## Features

- Automatically bold vocabulary words
- Collects words into a vocabulary section
- Alphabetically sorts entries
- Clickable hyperlinks back to the word in the notes
- Only first appearance is indexed

# Installation

Place `autovocab.sty` in:

- the same directory as your `.tex` file

or in your local TeX package directory.

Then include:

```latex
\usepackage{autovocab}
```

## Usage
### Add a vocabulary word
```latex
\vocab{homeostasis}
```

### Print the vocabulary list
```latex
\printvocabulary
```

Creates an alphebatized, default 3-column list of clickable links to the first reference of the vocab word. Use 
```latex
\printvocab[n]
```
to generate a n-column vocab list!

# Example
```latex
\documentclass{article}

\usepackage{autovocab}

\begin{document}

Cells maintain \vocab{homeostasis}.

The \vocab{mitochondria} produces ATP.

Molecules move by \vocab{diffusion}.

\clearpage

\printvocab

\end{document}
```