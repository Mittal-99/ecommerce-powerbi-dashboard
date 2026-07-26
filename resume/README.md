# Résumé — Anushi Mittal (Data & BI Analyst)

Single-page, ATS-friendly LaTeX résumé. Work experience is written in **STAR** format
(Situation → Action → Result), with a legend next to the section heading.

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
  block of `\sar{S} … \sar{A} … \sar{R} …` bullets.
- **Projects** — `\project{Name}{Context}{Year}`.
- **Keeping it to one page** — the layout is tuned to fill exactly one A4 page. If you add
  a bullet, remove one elsewhere, or loosen `\linespread{0.95}` / the `geometry` margins.
