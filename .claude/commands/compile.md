Use this command for the SilverStrand cover letter:

```powershell
Push-Location -LiteralPath 'C:\Users\zwang3\Documents\GitHub\ai-job-search\.claude\skills\job-application-assistant\Job_Applications\New Jobs 2026\SilverStrand'
try {
    xelatex -interaction=nonstopmode -file-line-error -halt-on-error Zhongli_Wang_Cover_Letter.tex
    Remove-Item -LiteralPath 'Zhongli_Wang_Cover_Letter.aux', 'Zhongli_Wang_Cover_Letter.log' -ErrorAction SilentlyContinue
} finally {
    Pop-Location
}
```

Do not compile this file from the repository root with an absolute `.tex` path, because LaTeX writes output files to the current working directory and the relative image paths will resolve incorrectly.

Use this command to transform the LaTeX source into a plain-text `.txt` file without LaTeX markup:

```powershell
Push-Location -LiteralPath 'C:\Users\zwang3\Documents\GitHub\ai-job-search\.claude\skills\job-application-assistant\Job_Applications\New Jobs 2026\SilverStrand'
try {
    pandoc --from=latex --to=plain --wrap=none 'Zhongli_Wang_Cover_Letter.tex' -o 'Zhongli_Wang_Cover_Letter.txt'
} finally {
    Pop-Location
}
```

If you want the `.txt` file to match the compiled PDF's visible text layer instead, compile the PDF first and then run:

```powershell
Push-Location -LiteralPath 'C:\Users\zwang3\Documents\GitHub\ai-job-search\.claude\skills\job-application-assistant\Job_Applications\New Jobs 2026\SilverStrand'
try {
    pdftotext -layout 'Zhongli_Wang_Cover_Letter.pdf' 'Zhongli_Wang_Cover_Letter.txt'
} finally {
    Pop-Location
}
```

Other pdf compilation commands:

pdflatex -interaction=nonstopmode -file-line-error                                                 

Use this command for the academic CV in `auto_cv_new`:

```powershell
Push-Location -LiteralPath 'C:\Users\zwang3\Documents\GitHub\ai-job-search\.claude\skills\job-application-assistant\Job_Applications\auto_cv_new'
try {
    pdflatex -interaction=nonstopmode -file-line-error -halt-on-error 'cv_wang_acade.tex'
    pdflatex -interaction=nonstopmode -file-line-error -halt-on-error 'cv_wang_acade.tex'
    Remove-Item -LiteralPath 'cv_wang_acade.aux', 'cv_wang_acade.bcf', 'cv_wang_acade.log', 'cv_wang_acade.out', 'cv_wang_acade.run.xml' -ErrorAction SilentlyContinue
} finally {
    Pop-Location
}
```

Do not compile this CV from the repository root with an absolute `.tex` path. Run from the `auto_cv_new` folder so `cv_wang_acade.pdf` is created there.

The CV contains a `biblatex` bibliography. If Biber works on your local shell and you need to refresh the bibliography section, use this fuller sequence:

```powershell
Push-Location -LiteralPath 'C:\Users\zwang3\Documents\GitHub\ai-job-search\.claude\skills\job-application-assistant\Job_Applications\auto_cv_new'
try {
    pdflatex -interaction=nonstopmode -file-line-error -halt-on-error 'cv_wang_acade.tex'
    biber 'cv_wang_acade'
    pdflatex -interaction=nonstopmode -file-line-error -halt-on-error 'cv_wang_acade.tex'
    pdflatex -interaction=nonstopmode -file-line-error -halt-on-error 'cv_wang_acade.tex'
    Remove-Item -LiteralPath 'cv_wang_acade.aux', 'cv_wang_acade.bbl', 'cv_wang_acade.bcf', 'cv_wang_acade.blg', 'cv_wang_acade.log', 'cv_wang_acade.out', 'cv_wang_acade.run.xml' -ErrorAction SilentlyContinue
} finally {
    Pop-Location
}
```
