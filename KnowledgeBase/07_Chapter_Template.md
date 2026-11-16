# Chapter Template

Copy this skeleton into `Chapters/ChapterN.tex` and replace the placeholders. Do not add `\begin{document}` or `\end{document}`.

```latex
% ATTENZIONE: Nei file secondari NON devi inserire \begin{document} o \end{document}.
\newpage

\chapterimage{Pictures/Indice.png}
\chapter{Chapter Title}\label{ch:short_label}

\section{Introduction}

State the problem, why it matters, and which lecture deck the chapter follows.
Cite the deck with \cite{...}.

\section{Core Theory}

\subsection{First Concept}

Define the concept, give the intuition, and write the equation in the body text.
Explain every symbol immediately after the equation.

\begin{Notebox}
\textbf{A caveat or practical warning.}
\end{Notebox}

\subsection{Second Concept}

Continue the argument. Use a figure when the lecture relies on a visual.

\begin{figure}[htbp]
    \centering
    \includegraphics[width=0.8\textwidth]{Pictures/example.png}
    \caption{What the figure shows.}\label{fig:example}
\end{figure}

\section{Worked Example}

\begin{examplebox}
\textbf{Step-by-step example.}
Write the numbers, the intermediate results, and the final answer.
\end{examplebox}

\section{Practical Notes}

Collect training recipes, implementation caveats, and trade-offs that appear in the slides.

\newpage
\section{Recap: Key Concepts}

One short paragraph that states the thread of the chapter.

\begin{table}[htbp]
\centering
\small
\renewcommand{\arraystretch}{1.15}
\begin{tabular}{p{0.20\textwidth} p{0.35\textwidth} p{0.33\textwidth}}
\toprule
\textbf{Concept} & \textbf{Key idea} & \textbf{Formula / rule} \\
\midrule
Concept 1 & One line of intuition & $formula$ \\
Concept 2 & One line of intuition & $formula$ \\
\bottomrule
\end{tabular}
\caption{One-page recap of the key concepts in this chapter.}\label{tab:chN_recap}
\end{table}

\begin{InsightBox}
\textbf{The one-sentence version:} the whole chapter in one sentence.
\end{InsightBox}
```

## Checklist for a new chapter

- [ ] The chapter follows the lesson map in `03_Lesson_Map.md`.
- [ ] Every technical concept from the deck is covered or explicitly declared out of scope.
- [ ] Every equation is explained at the lecture's level.
- [ ] At least one worked example is present if the lecture has one.
- [ ] The chapter ends with a recap table and a one-sentence `InsightBox`.
- [ ] No Markdown artifacts, no old conceptual roadmap, no removed FDS exercise.
- [ ] The chapter is included in `main.tex`.
- [ ] The PDF compiles and the new pages have been inspected.
