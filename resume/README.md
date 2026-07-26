# Résumé — Anushi Mittal (Data & BI Analyst)

Single-page, ATS-friendly LaTeX résumé. Every work-experience bullet follows the **STAR**
structure — situation, action, result — written as one flowing sentence rather than
labelled parts.

## Files

| File | Purpose |
| --- | --- |
| `Anushi_Mittal_Resume.tex` | Source |
| `Anushi_Mittal_Resume.pdf` | Compiled output (1 page, A4) |

## Build

```bash
pdflatex Anushi_Mittal_Resume.tex
```

Or upload the `.tex` to [Overleaf](https://overleaf.com) and hit Recompile.

Packages used (all standard TeX Live): `geometry`, `titlesec`, `enumitem`, `xcolor`,
`array`, `tabularx`, `hyperref`, `lmodern`. No icon fonts — contact details are plain
text so résumé parsers read them correctly.

## Section order

Summary → Work Experience → Technical Skills → Key Projects → Certifications → Education

## Customising

- **Accent colour** — `\definecolor{accent}{HTML}{1F4E79}` near the top.
- **Roles** — `\role{Title}{Company}{Location & scope}{Dates}` followed by an `itemize`
  block. Keep each bullet as: problem solved → what you built → measured result.
- **Projects** — `\project{Name}{Context}{Year}`. To make a project title clickable, wrap
  the name in `\href{url}{...}`, as the E-Commerce project does.
- **Keeping it to one page** — the layout is tuned to fill exactly one A4 page. If you add
  a bullet, remove one elsewhere, or loosen `\linespread{0.95}` / the `geometry` margins.
