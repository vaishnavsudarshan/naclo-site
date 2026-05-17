# Linguistics Olympiad Prep Site

A Quarto-based website for learning to solve problems from [NACLO](https://nacloweb.org), [NACLI](https://nacloweb.org), and [IOL](https://ioling.org).

## ✨ Features

- **Searchable problem library** — filter by year, competition, topic, and difficulty
- **Guided solutions** — expandable hints before full solutions
- **Linguistic commentary** — each solution explains the broader linguistic significance
- **LaTeX/PDF export** — compile the problem set into a printable book
- **Zero local install** — edit online at [github.dev](https://github.dev), build via GitHub Actions

## 🚀 Quick Start (fully online)

1. **Fork this repo** on GitHub
2. Go to **Settings → Pages** and set Source to **GitHub Actions**
3. Edit any `.qmd` file at `github.dev` (press `.` on the repo page)
4. Commit — the site builds automatically in ~2 minutes

## 📁 Project Structure

```
naclo-site/
├── _quarto.yml          # Site configuration
├── index.qmd            # Home page
├── topics.qmd           # Topic overview
├── resources.qmd        # Study guides and export instructions
├── problems/
│   ├── index.qmd        # Searchable problem listing
│   ├── _template.qmd    # Copy this to add new problems
│   ├── 2024/
│   │   └── swahili-verbs.qmd
│   └── 2023/
│       └── devanagari.qmd
├── topics/
│   ├── morphology.qmd
│   ├── phonology.qmd
│   └── ...
├── competitions/
│   ├── naclo.qmd
│   ├── nacli.qmd
│   └── iol.qmd
└── assets/
    ├── custom.scss      # Main theme
    └── custom.css       # Additional styles
```

## ➕ Adding a Problem

1. Copy `problems/_template.qmd` to `problems/YEAR/your-problem-slug.qmd`
2. Fill in the YAML front matter (title, date, categories, difficulty, etc.)
3. Write the problem text, hints, and solution
4. Commit — the listing pages update automatically via Quarto's listing feature

## 📚 Exporting to PDF / LaTeX Book

```bash
# Single problem
quarto render problems/2024/swahili-verbs.qmd --to pdf

# Full site as PDF
quarto render --to pdf
```

To compile as a LaTeX book, change `project.type` to `book` in `_quarto.yml` and add a `chapters:` list.

## 🤝 Contributing

Pull requests welcome! Please:
- Follow the template structure
- Include a complete solution with linguistic commentary  
- Add the problem to the correct year folder
- Tag with appropriate categories

## License

Problem statements © their respective competitions. Solutions and commentary are original content released under CC BY 4.0.
