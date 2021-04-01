# To create PDF file

## Initial setup

Get tex conversion from the markdown file:

```
pandoc ../../chapters/nielsen/index.md -o nielsen-body.tex --resource-path=../chapters/nielsen/
```

Remove any unnecessary items like buttons or trailing headings (`## Notes`). Then copy the tex headers from the template file, then update the metadata:

  * Title, author, affiliation
  * Date, DOI, any changes to copyright
  * Abstract, keywords, URL in href

## General edits to the tex file

1. Remove tightlist
2. Remove `sub` from each `section` to level it up one and add `*` to remove section numbering

## Figures

Change figures to follow this format:

```tex
\begin{figure}
  \includegraphics[width=\textwidth]{nielsen-fig1.jpg}
  \caption{Mexica New Year Ceremony in San Jose, California in March 2016.}
\end{figure}
```

Change videos to follow this format (note `caption*` and the `\wmturlcaption` command):

```tex
\begin{figure}
  \includegraphics[width=\textwidth]{play-video.png}
  \caption*{Video Example 1. Example of a dance from the 2016 Mexica New Year
  Ceremony in San Jose, California hosted by Calpulli Tonalehqueh. \wmturlcaption}
\end{figure}
```

If we use QR codes instead:

* Create redirect page (fix YouTube link from `embed` to `watch=`)
* Use screen shot from this page to create the QR codes: [QR Code generator library](https://www.nayuki.io/page/qr-code-generator-library)
* Set to create vector image  with a border of 1, then get a screen shot

```
\begin{figure}
  \centering
  \includegraphics[height=4cm]{qr-code.png}
  \caption*{Video Example 1. Example of a dance from the 2016 Mexica New Year
  Ceremony in San Jose, California hosted by Calpulli Tonalehqueh. \wmturlcaption}
\end{figure}
```

## Bibliography

1. Replace `\{:.hang\}` with ``
2. Check for invisible starting characters before `------` author names
3. Enclose bibliography in `\begin{hangparas}{15pt}{1}`
4. Use `\hangpara{15pt}{1}` with other hanging needs so that the spacing before other sections does not get mixed up

## Build the file

Use `xelatex` to build:

```
xelatex nielsen.tex
```

Remove any unnecessary files and send the PDF along for proofing.