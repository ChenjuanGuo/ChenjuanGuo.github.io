# Homepage Maintenance Notes

## Publications

The homepage publication list is maintained in `pages/publications.html`.

Use the compact homepage format:

```html
<li><span class="paper-authors">Author A, <strong>Chenjuan Guo</strong>, Author B:</span><span class="paper-title">Paper Title. <strong>VENUE</strong></span></li>
```

Keep the list grouped by year with:

```html
<li class="papers-year">2026</li>
```

Venue labels should be clean and short:

- Use conference or journal abbreviations only, e.g. `ICML`, `ICLR`, `KDD`, `AAAI`, `CVPR`, `ICDE`, `IJCAI`, `WWW`, `NeurIPS`, `PVLDB`, `TKDE`, `PACMMOD`, `VLDB Journal`, `Nature Communications`.
- Do not show volume, issue, article number, page numbers, or proceedings details on the homepage.
- Normalize `Proc. VLDB Endow. 18(2): 239-252` and similar entries to `PVLDB`.
- Normalize `IEEE Trans. Knowl. Data Eng. ...` to `TKDE`.
- Normalize `Proc. ACM Manag. Data ...` to `PACMMOD`.
- Normalize `VLDB J. ...` to `VLDB Journal`.
- Normalize `KDD (1)` to `KDD`.

Paper distinctions should be shown as badges after the venue:

```html
<strong>NeurIPS</strong> <span class="paper-note paper-note--spotlight">Spotlight</span>
<strong>CVPR</strong> <span class="paper-note paper-note--oral">ORAL</span>
```

Do not encode distinctions inside the venue name. For example, use `CVPR` plus an `ORAL` badge, not `CVPR Oral`.

## Local Build

For validation, run:

```bash
bundle exec jekyll build
```

GitHub Pages builds the site automatically after pushing. Local builds may add Linux platform entries to `Gemfile.lock`; do not commit those platform-only lockfile changes unless intentionally updating dependencies.
