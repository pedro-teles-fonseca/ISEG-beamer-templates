# ISEG Beamer templates

## About this project

This repository contains four beamer templates tailored for [ISEG](https://www.iseg.ulisboa.pt/aquila/instituicao/ISEG/?locale=en) students and faculty:

- An [introductory](https://github.com/pedro-teles-fonseca/ISEG-beamer-templates/tree/master/ISEG-beamer101-template) and didactic  template (see [pdf](https://github.com/pedro-teles-fonseca/ISEG-beamer-templates/blob/master/ISEG-beamer101-template/presentation.pdf))
 
- A template for [thesis presentations](https://github.com/pedro-teles-fonseca/ISEG-beamer-templates/tree/master/thesis-presentation-template) (see [pdf](https://github.com/pedro-teles-fonseca/ISEG-beamer-templates/tree/master/thesis-presentation-template/presentation.pdf))

- A template for [lecture slides](https://github.com/pedro-teles-fonseca/ISEG-beamer-templates/tree/master/lecture-slides-template) (see [pdf](https://github.com/pedro-teles-fonseca/ISEG-beamer-templates/tree/master/lecture-slides-template/presentationpdf))

- A [minimalist](https://github.com/pedro-teles-fonseca/ISEG-beamer-templates/tree/master/minimalist-template) multi-purpose template (see [pdf](https://github.com/pedro-teles-fonseca/ISEG-beamer-templates/tree/master/minimalist-template/presentation.pdf))
  
## About the templates

- The thesis presentation template has a field for advisor/supervisor name
- The lecture slides template has title and subtitle fields
- The introductory template has no TOC, no sections and no subsections
- The minimalist template is similar to the introductory template but has no text on the headline/footline
 
## Tl;dr instructions

1. Download or clone this repository

2. Choose a template

3. If you use citations, paste them in biblatex format in the references.bib file.

4. Edit the presentation.tex file

5. Compile the document (the bibliography, if used, should be compiled with biber)

6. You can find your presentation in the presentation.pdf file

## Detailed instructions

### Structure

I made the customizations on files that are called from the main tex file (presentation.tex) so that you only have to edit one file. Compiling presentation.tex will render a presentation in pdf format called presentation.pdf. You can find both these files in the template's main folder.

### Customization

In the presentation.tex file you need to edit the *title* and *author* fields. Uncomment the *subtitle* field if you want to use it. 

```tex
% Title and subtitle
%--------------------------------------------------------------
\title[Presentation Title]{Presentation Title}
%\subtitle{Presentation Subtitle}

% Your name
%--------------------------------------------------------------
\author[Your Name]{Your Name}

```
The name and title between the square brackets will be displayed on the footline of the frames and the name and title between curly brackets will be displayed in the title page. In the lecture slides template the subtitle field is uncommented by default.

In the thesis presentation template you also need to edit the advisor's name:

```tex
% Your name and advisor's name
%--------------------------------------------------------------
\author[Your Name]{Your Name \\ \footnotesize{\normalfont Advisor: Prof Dr. Your Advisor's Name}}
```

You can edit the date field. By default, the presentation will display the date when it was compiled:

```tex
% Date
%--------------------------------------------------------------
\date{\today}
```

If you are using the thesis or lecture slides template but you don´t want to print a TOC after the title slide, comment out or delete this frame:

```tex
% Frame - table of contents (can be commented out)
%--------------------------------------------------------------
\begin{frame}{Contents}
	\tableofcontents
\end{frame}
```

If you want your definitions and theorems to be numbered go to the preamble.tex file in the files folder and uncomment the following lines:

```tex
% \setbeamertemplate{theorems}[numbered]
% \setbeamertemplate{definitions}[numbered]
```

Build your frames after these commented lines:

```tex
%--------------------------------------------------------------
%--------------------------------------------------------------
%  Start building your frames here
%--------------------------------------------------------------
%--------------------------------------------------------------
```

This is what a typical frame looks like:

```tex
\begin{frame}{frame title}
    frame content
\end{frame}
```



### Citations

If you use citations, paste them in the references.bib file in biblatex format or replace references.bib with a file of the same name where you have your citations. I recommend using [Jabref](http://www.jabref.org) to organize your citations and generate bib files.

If you don't want to print the bibliography on the last slide, or if you don't use citations on your presentation, comment out or delete the inclusion of the references-section.tex file:

```tex
% Bibliography page (can be commented out)
%--------------------------------------------------------------
\include{files/references-section}
```

