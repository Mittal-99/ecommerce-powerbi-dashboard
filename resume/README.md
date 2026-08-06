# Résumé — Anushi Mittal (Data & BI Analyst)

Single-page, ATS-friendly LaTeX résumé. Every work-experience bullet follows the **STAR**
structure — situation, action, result — written as one flowing sentence rather than
labelled parts.

## Files

| File | Purpose |
| --- | --- |
| `Anushi_Mittal_Resume.tex` / `.pdf` | **General** Data & BI Analyst resume |
| `Anushi_Mittal_Solutions_Consultant.tex` / `.pdf` | Tailored for **Solutions Consultant** (Curlec by Razorpay) |

Both are one A4 page and share the same template and preamble. The tailored variant
reframes the same facts toward technical presales and solution delivery: it leads with the
"Solution Delivery Executive" title, foregrounds discovery, requirements, REST API
integration, onboarding and UAT, and regroups skills under Solution Consulting /
Integration & Architecture / Data & Analytics / AI & Productivity / Ways of Working.
Nothing is claimed that the general resume does not support.

## Build

```bash
pdflatex Anushi_Mittal_Resume.tex
pdflatex Anushi_Mittal_Solutions_Consultant.tex
```

Or upload the `.tex` to [Overleaf](https://overleaf.com) and hit Recompile.

Packages used (all standard TeX Live): `geometry`, `titlesec`, `enumitem`, `xcolor`,
`hyperref`, `lmodern`.

## ATS notes

The layout is deliberately parser-safe, verified with `pdftotext`:

- **Single column, no tables.** Dates align right via a justified `\hfill` line
  (`\headrow`), not a `tabular`, so extraction stays linear and in reading order.
- **No icon fonts, images, text boxes, headers or footers.**
- **Plain-text contact line** — email, phone and links are literal text, each also a
  live hyperlink.
- **Standard section names** in plain capitalisation, no small caps.
- **Text-mode glyphs only** — `\textbullet` for bullets and `--` for dashes; no
  math-mode symbols (a math `$\sim$` or `$\bullet$` can extract as noise).
- **Skills as `Category: item, item` lines**, the format parsers split most reliably.
- **PDF metadata** set: title, author, subject, language and keywords.

To re-verify after editing: `pdftotext Anushi_Mittal_Resume.pdf - | less`

## Section order

Summary → Work Experience → Technical Skills → Key Projects → Certifications → Education

## Customising

- **Accent colour** — `\definecolor{accent}{HTML}{1F4E79}` near the top.
- **Roles** — `\role{Title}{Company}{Location & scope}{Dates}` followed by an `itemize`
  block. Keep each bullet as: problem solved → what you built → measured result.
- **Projects** — `\project{Name}{Context}{Year}`. To make a project title clickable, wrap
  the name in `\href{url}{...}`, as the E-Commerce project does.
- **Skills** — `\skillline{Category}{comma, separated, items}`.
- **Keeping it to one page** — the layout is tuned to fill exactly one A4 page. If you add
  a bullet, remove one elsewhere, or loosen `\linespread{0.95}` / the `geometry` margins.

## Gaps against the Curlec / Razorpay JD

Deliberately **not** written into the tailored resume, because there is no evidence for
them and inventing them would not survive a screen:

- **Malay fluency** — a stated must-have for the role. No language line was added.
- **Mandarin** — listed as highly desirable.
- **Payments domain** — PCI DSS, tokenization, cards / e-wallets / FPX, the end-to-end
  payment lifecycle. The nearest genuine touchpoints are data reconciliation, REST API
  integration and the payment-method mix analysis in the e-commerce project.
- **Location / work authorisation** — the role is Malaysia-based.

Add a `Languages` line and any payments exposure if these apply.

## Parked content

Removed on request, kept here in case it goes back in later: the **Soft Skills** row
(Stakeholder Management, Requirements Gathering, UAT, Agile/Scrum, Cross-functional
Delivery) and the **Microsoft PL-300** and **AZ-900** certifications with their
associated Power BI Service and Azure skill lines.
