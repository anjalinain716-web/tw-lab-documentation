# LaTeX

## 1. Introduction

LaTeX is a document preparation system used to create professional and high-quality documents. It is widely used in academic, scientific, and technical writing.

Unlike traditional word processors, LaTeX uses markup commands to define the structure and formatting of a document.

It is especially useful for documents containing mathematical equations, tables, references, and technical content.

## 2. Features of LaTeX

- Produces professional-quality documents.
- Supports complex mathematical equations.
- Provides automatic numbering of sections, figures, and tables.
- Supports references and bibliographies.
- Handles large documents such as books, reports, and research papers.
- Provides consistent formatting.
- Supports multiple packages for additional functionality.

## 3. Basic Structure of a LaTeX Document

A basic LaTeX document follows this structure:

```latex
\documentclass{article}

\title{My First LaTeX Document}
\author{Student Name}
\date{\today}

\begin{document}

\maketitle

\section{Introduction}
This is my first LaTeX document.

\section{Conclusion}
LaTeX is useful for technical writing.

\end{document}
```

### Explanation

- `\documentclass{article}`: Defines the document type.
- `\title{}`: Specifies the document title.
- `\author{}`: Specifies the author's name.
- `\date{}`: Specifies the date.
- `\begin{document}`: Starts the document.
- `\maketitle`: Displays the title, author, and date.
- `\section{}`: Creates a section.
- `\end{document}`: Ends the document.

## 4. Document Classes

The `\documentclass{}` command defines the type of document.

Common document classes include:

| Document Class | Purpose |
|---|---|
| `article` | Articles and short reports |
| `report` | Reports and academic projects |
| `book` | Books and long documents |
| `letter` | Letters |
| `beamer` | Presentations |

Example:

```latex
\documentclass{article}
```

## 5. Sections and Subsections

LaTeX provides commands to organize content into sections.

Example:

```latex
\section{Introduction}

\subsection{Background}

\subsubsection{Overview}
```

These commands create a structured document with different heading levels.

## 6. Text Formatting

LaTeX provides commands for formatting text.

| Command | Purpose |
|---|---|
| `\textbf{Text}` | Bold text |
| `\textit{Text}` | Italic text |
| `\underline{Text}` | Underlined text |
| `\emph{Text}` | Emphasized text |
| `\texttt{Text}` | Monospaced text |

Example:

```latex
\textbf{Bold Text}

\textit{Italic Text}

\underline{Underlined Text}
```

## 7. Lists in LaTeX

LaTeX supports different types of lists.

### Unordered List

The `itemize` environment creates bullet lists.

```latex
\begin{itemize}
    \item First point
    \item Second point
    \item Third point
\end{itemize}
```

### Ordered List

The `enumerate` environment creates numbered lists.

```latex
\begin{enumerate}
    \item Introduction
    \item Features
    \item Conclusion
\end{enumerate}
```

## 8. Mathematical Equations

LaTeX is widely used for writing mathematical expressions.

### Inline Equation

```latex
The equation is $a^2 + b^2 = c^2$.
```

### Display Equation

```latex
\[
E = mc^2
\]
```

### Fraction Example

```latex
\[
\frac{a}{b}
\]
```

### Summation Example

```latex
\[
\sum_{i=1}^{n} i
\]
```

## 9. Tables in LaTeX

The `tabular` environment is used to create tables.

Example:

```latex
\begin{tabular}{|c|c|}
\hline
Name & Marks \\
\hline
Amit & 90 \\
Neha & 85 \\
\hline
\end{tabular}
```

Here:

- `c` represents center alignment.
- `l` represents left alignment.
- `r` represents right alignment.
- `\hline` creates a horizontal line.
- `&` separates columns.
- `\\` ends a row.

## 10. Adding Images

Images can be inserted using the `graphicx` package.

Example:

```latex
\usepackage{graphicx}

\begin{document}

\includegraphics[width=0.5\textwidth]{image.png}

\end{document}
```

The `\includegraphics` command inserts an image into the document.

## 11. Packages in LaTeX

Packages extend the functionality of LaTeX.

They are included using the `\usepackage{}` command.

Some commonly used packages are:

| Package | Purpose |
|---|---|
| `graphicx` | Inserting images |
| `amsmath` | Mathematical equations |
| `geometry` | Page layout and margins |
| `hyperref` | Adding hyperlinks |
| `xcolor` | Using colors |
| `array` | Advanced table formatting |

Example:

```latex
\usepackage{amsmath}
\usepackage{graphicx}
\usepackage{hyperref}
```

## 12. Cross-Referencing

LaTeX allows users to refer to sections, figures, and tables automatically.

Example:

```latex
\section{Introduction}
\label{sec:intro}

Refer to Section \ref{sec:intro}.
```

- `\label{}` assigns a reference name.
- `\ref{}` displays the corresponding number.

## 13. Bibliography and Citations

LaTeX supports citations and references in academic documents.

Example:

```latex
This topic is discussed in \cite{author2025}.

\begin{thebibliography}{9}

\bibitem{author2025}
Author Name,
Book Title,
2025.

\end{thebibliography}
```

The `\cite{}` command inserts a citation, while the `thebibliography` environment stores reference details.

## 14. Advantages of LaTeX

- Produces high-quality documents.
- Excellent mathematical typesetting.
- Automatically manages numbering and references.
- Suitable for large academic documents.
- Maintains consistent formatting.
- Supports reusable templates and packages.

## 15. Applications of LaTeX

LaTeX is commonly used for:

- Research papers.
- Academic assignments.
- Technical reports.
- Books and theses.
- Mathematical and scientific documents.
- Conference papers and presentations.

## 16. Conclusion

LaTeX is a powerful document preparation system used for creating structured, professional, and technically accurate documents. Its mathematical typesetting, automatic numbering, and reference management features make it especially useful in academic and scientific writing.