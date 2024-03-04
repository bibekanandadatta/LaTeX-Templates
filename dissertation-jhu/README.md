# JHU Dissertation Template

This is an unofficial Johns Hopkins dissertation template with recent updates by Bibekananda Datta. As of February 2024, the template follows the dissertation formatting requirements provided by the [Johns Hopkins University Sheridan Library](https://www.library.jhu.edu/library-services/electronic-theses-dissertations/formatting-requirements/). 

Johns Hopkins Library is flexible in terms of the format except for the title page, margins, and overall double-spaced content. Be sure to check it before you proceed any further. It is the user's responsibility to ensure all the formatting requirements are met.


## History of the template

- The report-class-based template was created by R. Jacob Vogelstein in May 2007
- Updated by Noah J. Cowan on March 1, 2010
- Updated by Brian D. Weitzner on April 29, 2014 
- Updated by John Muschelli on January 29, 2016 
- Updated by Leonardo Collado Torres on April 13, 2016 
- Updated by John Clayton in December 2019
- The current version is updated by Bibekananda Datta in February 2024



## What is included in the template

Since the template is based on the report class, it is subdivided into multiple chapters. For all the front matters (mandatory or optional), technical chapters, and back matters (references and appendices), there are separate .tex files. The `00-main.tex` file is the driver or root file which includes all the preamble, document settings, package settings, and macros as needed. I would recommend going through the different sections of this file to understand what are the options available. Compared to the previous version of the thesis template, the current version includes the following:

- Reorganization of the necessary packages (you may need more) and their settings.
- Modularized all the settings, formatting, and macros. You can add more as needed.
- Added specific settings for adding epigraphs before or after the chapter heading.
- Added settings to control the white space from the top of the chapter to the chapter heading.
- Added header option for each chapter. Will add a short header option for a larger chapter name.
- Updated the appearance of table of contents, list of figures, and list of tables.



## Some useful comments and suggestions for using the template

Please read the following suggestions before you start using the template:

- Some necessary variables to customize the formatting of the document are included at the beginning of the document. Understand what each variable does and change them as needed.
- The bibliography file is based on BibLaTeX which is a more modern package compared to BibTeX and natbib. Use Zotero (this is what I use) or some other citation manager to generate a standard BibLaTeX file.
- If your bib file name is different than the current file, then change it at the beginning of the document where all the variables are declared.
- Currently `apa` and `nature` style options are there for bibliography. Choose either of them or you can add something else depending on your field or department requirement or advisor's suggestion such as `IEEE` or something else. Find where the BibLaTeX package is added to the document and customize the options.
- Add all the figures in the `figures` subdirectory. You can add chapter-wise pdf files (which I prefer) or just add all of them as you have them.
- Decide if you will include any quote at the beginning of a chapter. If so, will it be placed before or after the chapter heading?
  - If you add a quote before the chapter heading, then all of your chapters will have some additional white space as it has now. (see, Chapter 2)
  - If you are using a quote after the chapter heading then you may want to reduce the white space before this. I like more compact formatting. (see, Chapter 3)
- For unnumbered chapters that you want to add to the table of contents, use the `\chap` command instead of the `\chapter*` command.
- Similarly for unnumbered sections, subsections, and subsubsections that you would like to add to the table of contents, use `\sect`, `\subsect`, and `\subsubsect` commands.
- Tables are defined to have `\arraystretch{1.5}` (equivalent to double space), but if you would like to customize it globally throughout the document, you can try decreasing/ increasing it. I suggest doing it locally by defining a group for each table (StackOverflow is your friend here).
- If the table is wider than the page, you may want to use the landscape tables which are placed sideways and may go over multiple pages (search online; someone on StackOverflow has done it).
- If the chapter name is too long, you may have to customize the header spacing in the geometry settings options to accommodate that. If it gets difficult to customize, you may want to remove all the header options. In the future, I plan on adding a short header option for long chapter names.
- Add more packages, customized macros, or maybe more chapters as needed. Happy Graduation!
