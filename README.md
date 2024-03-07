# LaTeX-Templates
 Collection of personal LaTeX templates for academic purposes. The collection contains a few directories (descriptions are given below). Users are welcome to clone/ fork/ download these templates. The templates were generated on Overleaf and compiled with `pdflatex`. I highly recommend using the templates in Overleaf. In case, you would like to do it locally, you may need to have all the necessary packages installed for error-free compilation.

If you are new to using LaTeX, these templates may be a bit overwhelming to you. I highly suggest going through the main files before using them. I generously commented on different sections of the scripts. Let me know if you clarification on something You are welcome to customize the templates to use for other purposes.


## How to use the repository and sub-directories

Currently all my LaTeX templates are contained in this repository. Even if you are interested in one particular subdirectories, you may have to clone or download the whole reopsitory (sorry about that). I just found it inefficient to manage multiple repositories for similar project. 

### Overleaf (vs. Local)

I personally highly recommend using [Overleaf](https://www.overleaf.com) for these projects. You can also do it locally on your computer. In that case, you may have to install a proper tex editor and tex compiler based on your system which is out-of-scope for now. I am assuming, you already have a tex system configured when you're using this templates (either on Overleaf or locally). Follow the following instructions

- Clone the repository to a specific location on your local computer. Alternatively, you can download the .zip file for this project.
- Once downloaded, unzip (if you downloaded) and navigate to the specific subdirectory.
- Compress the specific subdirectory you are interested in. Head to Overleaf. Click on New Project > Upload Project and then upload the subdirectory you compressed before.
- Alternatively, you can create a project on Overleaf and upload the files or subfolders directly to the project you created.
- Your project should be ready now. You can rename the project and start working on it.


## Description of the source code directories

- `article`: This is based on the LaTeX article class with the necessary packages to write a small to decent size article (up to a few 10s of pages). Users can add more packages and define more macros based on their needs. I use this template regularly for scientific writing.
- `report`: This is based on the LaTeX report class. This template can be used to create large technical reports containing multiple chapters. The directory contains a main file that includes all the preamble, macros, and formatting information with other necessary files dedicated to each chapter of the report. The preamble and formatting of this document are slightly more involved than the `article` template.
