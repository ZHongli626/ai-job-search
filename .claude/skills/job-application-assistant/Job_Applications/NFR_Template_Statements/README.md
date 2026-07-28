# LaTeX templates for NFR

This repository contains **_unofficial_** LaTeX templates for [Norges Forskningsråd](https://www.forskningsradet.no/) applications. This LaTeX template is based on the official Word template found [here](https://www.forskningsradet.no/siteassets/utlysninger/vedlegg-utlysninger/template-for-project-description-researcher-project-for-experienced-scientists-and-early-career-scientists.docx). It consists of a class file and four bibliography styles. The class file follows the following instructions in the official template:
> The page format must be A4 with 2 cm margins, single spacing and Arial, Calibri, Times New Roman or similar 11-point font. You are permitted to use 9-point font for the list of references and figure captions.
> 
The bibliography styles facilitate abbreviated bibliographies and citation styles (see below).

The class file (nfr.cls) contains the `nfr` LaTeX class. This is used in the "Template" file, which is a reproduction of the official NFR templates. The "Template" file is a conversion of the official file "Template for project description - Researcher project for experienced scientists and early career scientists.docx", converted to LaTeX by pandoc. I modified the "Template" file to use the nfr document class so that section A of that document is the actual structure, using the \section and \subsection commands, and the other sections are treated as an appendix.

In addition to general formatting, the class file also contains counters and commands for work packages (`\workpackage`), tasks (`\task`), deliverables (`\deliverable`), and milestones (`\milestone`), as well as reference commands (`\wpref`, `\tskref`, `\dref`, and `\mref`). These commands can collect duration information for automatic Gantt chart generation. See the file `Gantt_chart_example.tex` for a working example.

There are also counters and environments for objectives (`objective`), hypotheses (`hypothesis`), and research questions (`resq`). The environments have starred (`*`) alternatives which are not numbered. The number prefix can be changed by passing an alternative prefix as an option in brackets to the environment.

I have also included four bibliography styles to work with the natbib package in the `bst` directory. All four aim to reduce the length of the bibliography that's produced. The styles `shortnat` and `veryshortnat` are for author-year references, while `shortnum` and `veryshortnum` are for numbered references. See an example of how to produce Nature-like references in the "Template" file. The directory also contains versions of these styles with support for the [jabbrv package](https://github.com/compholio/jabbrv). They are prefixed with `jabbrv_`.

This template is maintained on github at [https://github.com/einola/NFR_template](https://github.com/einola/NFR_template). Feel free to fork it and make suggestions via pull requests to the original repository.
