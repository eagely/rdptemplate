# Diploma Thesis Template

A flexible LaTeX template for diploma theses, designed for HTL St. Pölten but adaptable for any institution.

## Requirements

- LaTeX distribution (TeXLive, MiKTeX, etc.)

## Structure

- **Title Page**: Customizable with your institution's details
  - Replace `assets/htl.png` and `assets/htl-bbs.png` with your logos
  - Customize header info with `\school`, `\department`, etc.
- **Affidavit**: Includes
  - Signature fields for each candidate
  - Individual task descriptions
- **Time Tracking**: Built-in system for project hours
  ```latex
  \addtimeentry{Week Number}{Task Description}{Hours}
  ```
  - Automatically sorts entries by year (2024/2025)
  - Calculates total hours
  - Print the table with `\printtimeentries`
- **Bibliography**: BibLaTeX with numeric citation style
  - Add references to `references.bib`
  - Cite using `\cite{key}`

## Configuration

Edit these fields in your main.tex:
```latex
\documentclass[paper=a4, 12pt,oneside]{scrbook}
\usepackage{rdp}
\usepackage[scale=0.72, twoside, bindingoffset=2mm]{geometry}

\school{HTBLuVA St. Pölten}
\department{Higher Institute for Electronics and Technical Informatics}
\subdepartment{Specializations in Embedded and Wireless Systems}
\session{2025/26}
\title{Title}
\subtitle{Add subtitle}
\note{Licensed under ___}
\supervisor{Supervisor 1}
\supervisor{Supervisor 2}
\candidate{Name 1}{Task 1}
\candidate{Name 2}{Task 2}
\place{St. Pölten}
\handindate{04.04.2025}
```

For single-sided layout, remove `twoside`:
```latex
\usepackage[scale=0.72]{geometry}
```

## Content Organization

Place your content files in the `topics/` directory and include them in main.tex:
```latex
\include{topics/introduction}
\include{topics/results}
\include{topics/time}
\include{topics/bibliography}
```

## License

CC0 - see [LICENSE](LICENSE)
