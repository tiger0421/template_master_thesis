# template_master_thesis
CIT 2021 template of master thesis

## Example


```
.
├── main.tex
└── tex
    ├── title.tex
    └── background.tex
```

main.tex
```tex
\documentclass[autodetect-engine, a4paper, 11pt, oneside]{jsbook}

\makeatletter 
\def\input@path{{../}} 
\makeatother

\input{thesis_settings.tex}

\begin{document}
  \linesparpage{26}

  \subfile{tex/title.tex}

  \tableofcontents
  \listoffigures
  \listoftables
  \linesparpage{30}
  \newpage
    
  \subfile{tex/background.tex}
\end{document}
```

title.tex
```tex
\documentclass[../main]{subfiles}

\setcounter{section}{1}
\begin{document}
  \begin{titlepage}
    \begin{center}
      {\huge  修士論文}\\
      \vspace{2cm}
      {\huge タイトル}\\
      \vspace{1cm}
      {\huge Title}\\
      \vspace{4cm}
      {\huge The instructor}\\
      \vspace{2cm}
      {\LARGE \today}\\
      \vspace{1cm}
      {\LARGE Course of study}\\
      \vspace{1cm}
      {\LARGE author}\\
    \end{center}
  \end{titlepage}
\end{document}
```

background.tex
```tex
\documentclass[../main]{subfiles}

\setcounter{section}{1}
\begin{document}
  \chapter{Background}
\end{document}
```
