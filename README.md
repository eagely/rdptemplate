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

## Configuration

Edit these fields in your main.tex:
```latex
\school{School Name}
\department{Department Name}
\subdepartment{Subdepartment}
\session{2025/26}
\title{Your Title}
\subtitle{Your Subtitle}
\place{Location}
\handindate{04.04.2025}
\supervisor{Supervisor 1}
\supervisor{Supervisor 2}
\candidate{Name 1}{Task 1}
\candidate{Name 2}{Task 2}
```

## Layout

Default is two-sided (for printing):
```latex
\usepackage[scale=0.72, twoside, bindingoffset=2mm]{geometry}
```

For single-sided:
```latex
\usepackage[scale=0.72]{geometry}
```

## License

CC0 - see [LICENSE](LICENSE)
