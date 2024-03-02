# JHU Dissertation Template

This is an unofficial Johns Hopkins dissertation template with recent updates by Bibekananda Datta. As of February 2024, the template follows the dissertation formatting requirements provided by the [Johns Hopkins University Sheridan Library](https://www.library.jhu.edu/library-services/electronic-theses-dissertations/formatting-requirements/). Be sure to check it before you proceed any further.


## History of the template

- The report-class-based template was created by R. Jacob Vogelstein in May 2007
- Updated by Noah J. Cowan on March 1, 2010
- Updated by Brian D. Weitzner on April 29, 2014 
- Updated by John Muschelli on January 29, 2016 
- Updated by Leonardo Collado Torres on April 13, 2016 
- Updated by John Clayton in December 2019
- The current version is updated by Bibekananda Datta in February 2024



## What is included in the template

Since the template is based on the report class, it is subdivided into multiple chapters. For all the front matters (mandatory or optional), technical chapters, and back matters (references and appendices), there are separate .tex files. The `00-main.tex` file is the driver or root file which includes all the preamble, document settings, package settings, and macros as needed. I would recommend going through the different sections of this file to understand what are the options available. Compared to the previous version of the thesis template, the current version includes the following
- Reorganization of the necessary packages (you may need more) and their settings.
- Modularized all the settings, formatting, and macros. You can add more as needed.
- Added specific settings for adding epigraphs before or after the chapter heading.
- Added settings to control the white space from the top of the chapter to the chapter heading.
- Added header option for each chapter. Will add a short header option for a larger chapter name.
- Updated the appearance of table of contents, list of figures, and list of tables.



## How to use this template

I personally highly recommend using [Overleaf](https://www.overleaf.com) for these projects. You can also do it locally on your computer. In that case, you may have to install a proper tex editor and tex compiler based on your system which is out-of-scope for now. I am assuming, you already have a tex system configured when you're using these templates (either on Overleaf or locally). Follow the following instructions

- Clone the repository to a specific location on your local computer. Alternatively, you can download the .zip file for this project.
- Once downloaded, unzip (if you downloaded) and navigate to the specific subdirectory.
- Compress the specific subdirectory you are interested in. Head to Overleaf. Click on New Project > Upload Project and then upload the subdirectory you compressed before.
- Alternatively, you can create a project on Overleaf and upload the files or subfolders directly to the project you created.
- Your project should be ready now. You can rename the project and start working on it.
