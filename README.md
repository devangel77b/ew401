# es200-latex

This repository contains USNA ES200 Introduction to Systems Engineering course materials, mostly in Latex and C. It is revision controlled using git. To obtain a clone of these materials do one of the following:
```bash
git clone https://github.com/devangel77b/es200
git clone ssh://git@github.com/devangel77b/es200.git
```
The repository is currently set to private. For USNA WSE staff, Evangelista can set you as a collaborator to be able to access, pull, and push changes; please provide your github username. 

The repository makes use of git-lfs extensions for graphics and other resources, so be sure this is installed on your machine. 

My intention is to do tagged versions at each semester to aid in archiving course material for audit and accreditation purposes. To support this, if you plan to work on changes, please coordinate via the Github issue tracker and work in a new branch or a fork and send me a pull request (like proper software multi-programmer editing process), or work in the dev branch (which is where I work on new features). 

After cloning the directory, copy the course.sty.example file to course.sty:
```bash
cp course.sty.example course.sty
```
You should then edit the course.sty file to list your own name as the instructor, change the institution, course number, course name, assignment due dates etc. 

### Compiling the course materials in LaTeX

The materials are compiled using LaTeX.  On Windows machines, you will want to install Miktex.  On Linux Ubuntu machines, I use the Texlive distributions.  I have found Emacs and Texworks to be decent editors that are available on most machines.  

The Linux distribution will need to have a few packages installed, including: siunitx, graphicx, beamer, tufte-latex, lstlisting, (a few others?)  Miktex instalations on Windows machines should automatically install missing ones as it realizes they are missing.  Texlive installations seem to have these already. 

The directory structure should allow all the files to see the main course.sty options file where instructor name, course name and number, dates, etc are set. Relative addressing for references and figures should also already be handled (see example files for examples). The materials are already in a file structure for admin, hw, lectures, etc.  To compile a handout should just be the standard LaTeX sequence, for example:
```bash
cd course/hw/1/
pdflatex hw1
pdflatex hw1
pdflatex hw1
bibtex hw1
pdflatex hw1
```

### Rationale for LaTeX

LaTeX was used for all engineering course materials when I was an undergrad; it is an old and stable system well suited to this task. Use of git with LaTeX allows a revision controlled, backed up repository that can be cloned, versioned, forked, etc as necessary; and use of the git-lfs extensions allows all of the figures to be bundled too.  ES200 and the like require lots of code and equations which are much more graceful to do here in LaTeX; autoformatting the code is simple. USNA network outages have shown that total reliance on Google Drive or network drives can cause problems when access is lost. LaTeX should not be burdensome for code-capable engineers to use as it is already required for submission to many engineering journals. 

Personally, I have found that ITSD changes in version between various Office products alters the look and layout of slides and text and makes some legacy course material illegible. In addition, Google Drive posting on the .doc and .ppt files sometimes left out things like equations or chunks of text. I have not had these problems with PDF output created using LaTeX. 

There is peer-reviewed literature about the dangers and limitations of Powerpoint and its role in some major engineering disasters. I am attempting to use more Tufte-like notes and materials to move away from bullet point engineering and bad habits and cognitive styles enabled by Powerpoint. 

### Known issues

1. I'm still deciding if I prefer to do .svg in which inline Latex is handled through Latex or not. That feature works fine on Texlive installs but is difficult to configure on Miktex/Windows machines because it requires Inkscape be callable by Latex. 
1. There's a directory for book type materials but it has not yet been filled in to the same extent as the ES202 course materials. It will be eventually. 
1. Other issues (e.g. fair use) are noted in the online issue tracker in Github.
1. My Fall 2017 course policy file policy.tex currently uses a navy memo class developed by Evangelista that is not bundled within this repository. I'll have to track down where I have that one on github. 


