# LaTeX-Templates

This is a collection of personal LaTeX templates for academic purposes. The collection contains a few directories (descriptions are given below). Users are welcome to clone/ fork/ download these templates. The templates were generated on Overleaf and compiled with `pdflatex` compiler. I highly recommend using the templates in Overleaf (see below).

If you are new to using LaTeX, these templates may be a bit overwhelming to you. I highly suggest going through the main files of the repository you are interested in before using them. I generously commented on different sections of the scripts. Let me know if you clarification on something You are welcome to customize the templates to use for other purposes.


## Compiling on Overleaf

Currently, all my regular LaTeX templates are contained in this repository. Even if you are interested in one particular subdirectory, you may have to clone or download the whole repository (sorry about that). I just found it inefficient to manage multiple repositories for similar projects. I personally highly recommend using [Overleaf](https://www.overleaf.com) for these projects. They were generated and tested on Overleaf. You can also do it locally on your computer. In that case, you may have to install a proper text editor and latex compiler based on your system. However, I am assuming, you already have a tex system configured (local or Overleaf) when you're using these templates (either on Overleaf or locally). Follow the following instructions

- Clone the repository to a specific location on your local computer. Alternatively, you can download the .zip file for this project.
- Once downloaded, unzip (if you downloaded) and navigate to the specific subdirectory.
- Compress the specific subdirectory you are interested in. Head to Overleaf. Click on New Project > Upload Project and then upload the subdirectory you compressed before.
- Alternatively, you can create a project on Overleaf and upload the files or subfolders directly to the project you created.
- Your project should be ready now. You can rename the project and start working on it.


## Description of the source code directories

### article

This template shares similarities with [JHU MechE dissertation proposal template](https://github.com/bibekananda-datta/JH-MechE-Dissertation-Proposal-Template). You can find more details about the template there.

- This is based on the LaTeX article class with the necessary packages to write a small to decent-sized article (up to a few 10s of pages). Users can add more packages and define more macros based on their needs. I use this template regularly for scientific writing.

- Most of the necessary variables to manage the formatting of the document have been declared at the beginning of the `.tex` files. If you prefer customizing the format, you will likely find the necessary variable there. But you are welcome to add more variables and settings in the document to your preference or need. Add all of your figures to the main directory. You can also add the figures to a specific subdirectory if you would like. In that case, you will have to define the subdirectory using the `\includegraphicspath{}` command.

- The bibliography file is based on BibLaTeX which is a more modern package compared to BibTeX and natbib. Use Zotero (this is what I use) or some other citation manager to generate a standard BibLaTeX file.
  - Currently `nature` (numbered format) and `apa` (author-year format) style options are there for the bibliography. Choose either of them or you can add something else depending on your discipline or department requirement or advisor's suggestion such as IEEE, MLA, Harvard, Chicago, etc. Find where the BibLaTeX package is added to the document and customize the options for the bibliographic package based on the style.

- I used Latin Modern Roman font (loaded using the `lmodern` package) for the document as it produces consistent typography for text and math environment. If you prefer, you can use some other font by loading that package using the `\usepackage{}` command. However, you will have to be careful about the consistency of the typography, especially between text and math environments. [Follow this discussion on StackExchange to learn more about fonts in LaTeX](https://tex.stackexchange.com/questions/59702/suggest-a-nice-font-family-for-my-basic-latex-template-text-and-math).

- The margin used in both documents is **1.0in** for all sides with no header and footer except for the pagination at the bottom center inside the margin. If you would like to change it, then look for the `\geometry{}` command inside the `DOCUMENT FORMATTING` section.

- The main text sections of both documents are **single-spaced**. If you find the main text is too tightly spaced, you can space out the content by using `\onehalfspacing` or `\doublespacing` instead of `\singlespacing` for the main text in both .tex files. In this case, you will have to change the spacing for other environments as well to have a consistently formatted document. Most of the necessary variables that can customize the format of the template are declared at the very beginning of the .tex files. Tweak them to obtain more consistent formatting for the tables, figures, paragraphs, bibliographic items, etc. You are welcome to define more customized preamble settings as well.
  - In case you change text spacing, you most likely would need to change the spacing around the headings of different environments that are managed by the `parskip` package. I found the default settings to be working fine for me. But if you would like to customize it, you can add the following command in the preamble:
  ```
  \titlespacing*{<environment-name>}{<space-left>}{<space-before>}{<space-after>}
  ```

- If you find all the packages and their settings and macros to be overwhelming and distracting during the editing process, you can cut and paste all these contents to a separate `my-preamble.tex` file (name it as you like) in the project directory. Then you can use the command `input{my-preamble.tex}` to make your main file appear cleaner and less distracting. `\input{}` command pastes content from the source file. See [managing the large project on Overleaf](https://www.overleaf.com/learn/latex/Management_in_a_large_project).

- Add your math macros and settings in the `MATH SETTINGS AND MACROS` section. There's a section for non-math `OTHER MACROS` as well. Some examples of both types of macros are added there.
 
- If you would like to use colors in your writing or drawing, you can consider using the `xcolor` package with the `dvipsnames` option (already added in the preamble). Check [how to use colors in LaTeX on Overleaf](https://www.overleaf.com/learn/latex/Using_colors_in_LaTeX).


### beamer




### report

This template shares similarities with [JHU dissertation template](https://github.com/bibekananda-datta/JHU-Dissertation-Template). You can find more details about the template there.

- This is based on the LaTeX report class which uses a chapter-wise arrangement of the document. The directory contains a main file `(00-main.tex)` which you need to compile to generate the report. The main file includes a separate `my-preamble.tex` file which is added using `\input{}` command. This preamble file includes all the necessary packages and settings for document formatting. Most of the necessary settings for document formatting are declared as variables at the beginning of the `00-main.tex` file. Most likely, you can make changes there to obtain your preferred format. In the main document section of the `00-main.tex` file, different chapters are added using the `\include{}` command.

- In addition to the formatting-related variables, if your bib file has a different name than the current file, then change the `BibFileName` variable. Make sure to specify the correct name for the `graphicspath` as well.

- I used the Latin Modern Roman font (loaded using the `lmodern` package) for the document typeset in LaTeX because the text and math environments have consistent typesetting. You can try other fonts, but you should be careful about being consistent, especially for math and text typesettings. [Follow this discussion on StackExchange to learn more about fonts in LaTeX](https://tex.stackexchange.com/questions/59702/suggest-a-nice-font-family-for-my-basic-latex-template-text-and-math).

- Add all the figures in the `figures` subdirectory. If your subdirectory name is different, then change the `FigurePath` variable. You can add chapter-wise PDF files (which is what I prefer) or just add all of them as you have them in that directory.

- The bibliography file is based on BibLaTeX which is a more modern package compared to BibTeX and natbib. Use Zotero (this is what I use) or some other citation manager to generate a standard BibLaTeX file.
  - Currently `nature` (numbered format) and `apa` (author-year format) style options are there for the bibliography. Choose either of them or you can add something else depending on your discipline or department requirement or advisor's suggestion such as IEEE, MLA, Harvard, Chicago, etc. Find where the BibLaTeX package is added to the document and customize the options for the bibliographic package based on the style.

- The margin used in both documents is **1.0in** for all sides with no header and footer except for the pagination at the bottom center inside the margin. If you would like to change it, then look for the `\geometry{}` command inside the `DOCUMENT FORMATTING` section.
  - The title page does not have any pagination. You can customize the title page easily based on your needs or preferences. The pagination counter starts from the abstract page with the Roman numeral ii. For the main text in the proposal document, the pagination resets in Arabic starting from 1.
  - If the chapter name is too long, you may have to customize the header spacing in the geometry settings options to accommodate that. Tweak the variables `HeaderHeight` and `HeaderSpace` in the variable declaration section. You can add the `showframe` option to the `geometry{}` command to see the layout of your document.
  - If you have one or two chapters with long titles, changing it locally for individual chapters is a bit tricky task. In that case, you can use a header with a short chapter title option. See the examples given in individual chapters on how to add a shorter title. But if it gets difficult to customize or generalize, you can also consider removing all the header options by commenting them out in the document section of the `00-main.tex` file.

- The most common and popular packages for writing the report are added in the `LaTeX CLASS AND PACKAGES` sections. Check the packages; add any additional package you need and/or customize your options there.

- If you want to add a quote before the chapter heading, then you may want to increase the white spacing on top. In this case, all of the Chapters will have white space before Chapter # and title. I did not like the default font size and spacing in the LaTeX `report` class. 

- For unnumbered chapters that you want to add to the table of contents, use the `\chap` command instead of the `\chapter*` command. (see, *Preface* for example). Similarly, for unnumbered sections, subsections, and subsubsections that you would like to add to the table of contents, use `\sect`, `\subsect`, and `\subsubsect` commands, respectively. If you do not any of these environments to be added to the table of contents, then you can use standard * environments; such as `\section*{}`, etc.

- Currently, 3 numbered environments `\section{}`, `\subsection{}`, and `\subsubsection{}` are activated throughout the document and available in the table of contents. You can decrease or increase this by tweaking variables: `\NoSectionLevel` and `\NoTocLevel`. I prefer 2-3 levels for large documents, otherwise, it gets too clumsy and confusing.

- The main text sections of both documents are **single-spaced** except the table of contents, list of figures, and list of tables being **one-half-spaced** in `main.tex`. If you find the main text is too tightly spaced, you can space out the content by using `\onehalfspacing` or `\doublespacing` instead of `\singlespacing` for the main text in both .tex files. In this case, you will have to change the spacing for other environments as well to have a consistently formatted document. Most of the necessary variables that can customize the format of the template are declared at the very beginning of the .tex files. Tweak them to obtain more consistent formatting for the tables, figures, paragraphs, bibliographic items, etc. You are welcome to define more customized preamble settings as well.
  - In case you change text spacing, you most likely would need to change the spacing around the headings of different environments that are managed by the `parskip` package. I found the default settings to be working fine for me. But if you would like to customize it, you can add the following command in the preamble:
  ```
  \titlespacing*{<environment-name>}{<space-left>}{<space-before>}{<space-after>}
  ```

  
- Add your math macros and settings in the `MATH SETTINGS AND MACROS` section. There's a section for non-math `OTHER MACROS` as well. Some examples of both types of macros are added there.
 
- If you would like to use colors in your writing or drawing, you can consider using the `xcolor` package with the `dvipsnames` option (already added in the preamble). Check [how to use colors in LaTeX on Overleaf](https://www.overleaf.com/learn/latex/Using_colors_in_LaTeX).



## Contributing to these repositories

These repositories are licensed under MIT license. You are free to clone/ download/ fork these repositories and make changes by yourself. However, if you have any suggestions that you would like to see in these repositories, please let me know or make a `pull request`. I will review and incorporate them.

## Citation

If you use any of these templates in situations where it requires providing citations, please cite the repository.
