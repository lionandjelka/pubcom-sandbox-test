# ISSC PubCom — Converting LaTeX or PDF manuscripts to reviewable Markdown

**Purpose.** This is an optional technical guide for creating `manuscript_v1.md` alongside an authoritative `manuscript_v1.pdf`. The **current mock review uses both formats**, but PubCom has not decided whether Markdown will be mandatory for real papers. See [README.md](README.md) and [REVIEW_PROTOCOL.md](REVIEW_PROTOCOL.md).

**Use the source manuscript if possible.** Converting LaTeX to Markdown is usually more reliable than extracting text from the formatted PDF. Neither path guarantees faithful preservation of mathematics, figures, tables or references; the author (or designated conversion helper) must check the result before review.

## Method A — LaTeX (`.tex`) → Markdown (preferred)

### A1. Download the LaTeX source from Overleaf

1. Open the project in Overleaf.
2. Select **Menu → Download → Source** (wording may vary).
3. In Finder, double-click the downloaded ZIP to extract it.
4. Identify the main file (`main.tex`, `paper.tex` or similar), the `.bib` file, any `sections/*.tex`, and custom commands such as `\newcommand`.
5. If the project contains multiple `\input{...}` or `\include{...}` sources, check the converted manuscript for missing sections. Complex projects may require consolidating or adjusting the sources first.

### A2. Install Pandoc on macOS

Option 1: use the installer at <https://pandoc.org/installing.html>.

Option 2: if Homebrew is installed, run:

```bash
brew install pandoc
```

Confirm installation in Terminal:

```bash
pandoc --version
```

### A3. Open Terminal in the manuscript folder

In macOS Terminal, type `cd ` (with a trailing space), drag the extracted project folder from Finder into Terminal, and press Return. This avoids having to type the entire directory path.

### A4. Convert the main LaTeX file

```bash
pandoc main.tex \
  --from=latex \
  --to=gfm+tex_math_dollars \
  --wrap=none \
  --output=manuscript_v1.md
```

Replace `main.tex` with the actual main file. A `.md` file is created in the same working directory.

Optional bibliography processing (only when citations are supported by the source structure):

```bash
pandoc main.tex \
  --from=latex \
  --to=gfm+tex_math_dollars \
  --citeproc --bibliography=references.bib \
  --wrap=none \
  --output=manuscript_v1.md
```

**Bibliography caution:** Pandoc may not understand manuscript-specific bibliography macros, journal `.bst` formats, citation aliases or custom AASTeX macros. Check that in-text citations and bibliography entries remain meaningful. Do not assume `--citeproc` reproduces the journal's final reference layout.

### A5. Review the converted Markdown before submitting

Open `manuscript_v1.md` in a text editor or in GitHub's Markdown preview. Compare it to the PDF: check abstract, headings, equation symbols, mathematical signs, image references, tables, citations, footnotes and section order. If conversion is imperfect, keep the PDF as authoritative and label the Markdown a **review convenience copy**.

A GitHub-compatible example:

```markdown
## 3. Period search

The frequency estimate is obtained from the periodogram.

$$
P(\omega) = \frac{1}{2}\left[\frac{C^2}{CC} + \frac{S^2}{SS}\right].
$$
```

This equation is merely an illustrative formatting example, not a claim that all custom LaTeX environments will render correctly.

## Method B — PDF → Markdown (when no source is available)

**Pandoc does not directly read PDF as an input format.** First extract the PDF content using a PDF-aware converter. A practical local method is PyMuPDF4LLM. It generally works best with a text-based PDF; complex equations, two-column ordering and figures may need manual correction.

### B1. Install a PDF-to-Markdown converter

On a Mac with Python 3 installed, open Terminal and run:

```bash
python3 -m pip install --upgrade pymupdf4llm
```

If macOS/Python reports an externally-managed environment, use a virtual environment instead:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pymupdf4llm
```

### B2. Save a short Python script in the same folder as your PDF

Create `pdf_to_md.py` with:

```python
from pathlib import Path
import pymupdf4llm

source = Path("manuscript_v1.pdf")
output = Path("manuscript_v1.md")

md_text = pymupdf4llm.to_markdown(str(source))
output.write_text(md_text, encoding="utf-8")
print(f"Created {output.resolve()}")
```

Run:

```bash
python3 pdf_to_md.py
```

If you activated a virtual environment, use `python pdf_to_md.py` instead. Check that the generated `manuscript_v1.md` exists.

### B3. Alternative without Python scripting

If you already have a reliable PDF-to-Word conversion tool (for instance Acrobat or your institution's PDF service), export a **local DOCX**, inspect it for errors, then use Pandoc:

```bash
pandoc manuscript_v1.docx --from=docx --to=gfm+tex_math_dollars \
  --wrap=none --output=manuscript_v1.md
```

This is a fallback, not a fidelity guarantee. Avoid third-party online converters for any nonpublic manuscript, proprietary Rubin data, sensitive referee material or other restricted content unless specifically authorized.

### B4. When not to rely on PDF extraction

- **Scanned / image-only PDF:** ordinary text extraction may yield nothing; OCR may be needed and mathematical OCR errors are common.
- **Two-column layouts:** paragraphs, captions and footnotes can be interleaved.
- **Equations and symbols:** minus signs, Greek letters, exponents and subscripts may be corrupted.
- **Figures and tables:** Markdown may contain placeholders or reordered cells; the PDF remains the visual reference.
- **References:** verify order and citations manually.

## Quality-control checklist for scientific manuscripts

Before asking reviewers to comment on Markdown, the Author or designated conversion helper should verify:

- [ ] Title, abstract and complete section structure match the PDF.
- [ ] Units, symbols, indices, equations, inequalities and signs are intact.
- [ ] Important tables have correct row/column order and footnotes.
- [ ] Figure callouts and captions are traceable to the PDF.
- [ ] Citations, bibliography and author list are not silently altered.
- [ ] The Markdown is readable in GitHub **Files changed**.
- [ ] The PDF and Markdown carry the same explicit version/date.
- [ ] If the Markdown omits content, its header explains what to consult in the PDF.
- [ ] The source material may legally be stored in the chosen GitHub repository.

## Uploading the two files to the same Pull Request

1. Open the **paper's branch**, never `main`.
2. Navigate to `Publications/<paper-slug>/`.
3. Choose **Add file → Upload files**; select `manuscript_v1.pdf` and `manuscript_v1.md` (plus `summary.md` if not already present).
4. Commit the files **to the current publication branch**.
5. Open the existing Draft PR or create one against `main`. Verify that both manuscript versions appear in **Files changed**.
6. For revisions, add `manuscript_v2.pdf` and `manuscript_v2.md` **to the same PR branch** and update the revision table in `summary.md`; do not open a second PR for the same paper.

In the PR description, link to the file using its real GitHub URL (`.../blob/<branch>/Publications/.../manuscript_v1.pdf`). Avoid bare relative links that might redirect to **Compare changes**.

## If conversion is too difficult

Do **not** spend days forcing a complicated AASTeX manuscript into Markdown for the sake of this pilot. Tell the Paper Handler what failed. The committee is testing an alternative **PDF-only manuscript plus consolidated reviewer report**, with numbered reviewer requests and point-by-point author responses tracked in PR Conversation. This remains a **proposed format**, not an approved replacement for the current mock exercise.

## References

- Pandoc install: <https://pandoc.org/installing.html>
- Pandoc manual: <https://pandoc.org/MANUAL.html>
- PyMuPDF4LLM project: <https://github.com/pymupdf/pymupdf4llm>
- GitHub PR review guidance: <https://docs.github.com/en/pull-requests/get-started/reviewing-pull-requests-quickstart>
