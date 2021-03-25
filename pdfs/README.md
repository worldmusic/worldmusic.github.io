```
documentclass: scrartcl
classoption:
 - twocolumn
```

Make tex file

pandoc ../chapters/nielsen/index.md -s -o nielsen.tex --resource-path=../chapters/nielsen/

Replace `\{:.hang\}` with ``

xelatex nielsen.tex

Problems with figures/captions

## Try getting just the body

* Get body tex file with `pandoc ../chapters/nielsen/index.md -o nielsen-body.tex --resource-path=../chapters/nielsen/`
* add headers
* remove tightlist
* remove `sub` from each `section` to level it up one
* Change figures to

```
\begin{figure}
  \includegraphics[width=\textwidth]{nielsen-fig1.jpg}
  \caption{Mexica New Year Ceremony in San Jose, California in March 2016.}
\end{figure}
```

* Change videos to (note `caption*`)

\begin{figure}
  \includegraphics[width=\textwidth]{play-video.png}
  \caption*{Video Example 1. Example of a dance from the 2016 Mexica New Year
  Ceremony in San Jose, California hosted by Calpulli Tonalehqueh}
\end{figure}

## Next steps

* Remove indents from resources/readings/etc or change formatting
* Remove section numbering
* Fix bibliography hanging
* Add author info and abstract/tags
* Add headings
* Add branding, ISSN, DOI