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

* Fill in info (including author affiliations with `author`)
* Get body tex file with `pandoc ../chapters/nielsen/index.md -o nielsen-body.tex --resource-path=../chapters/nielsen/`
* add headers
* Add author info and abstract/tags
* remove tightlist
* remove `sub` from each `section` to level it up one and add `*` to remove section numbering
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
* Fix bibliography hanging
* Add headings
* Add branding, ISSN, DOI