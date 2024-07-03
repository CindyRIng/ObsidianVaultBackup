---
tags:
  - 工具/Tex
  - 工具/LaTex
  - year/2024
date: 2024-07-02 17:35:32
---
# Structure of LaTex
---
## Front Main and Backmatter

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=71&selection=81,1,105,83&color=yellow|p.I-26]]
> n LaTEX’s book class these three regions can be explicitly marked up using the commands \frontmatter, \mainmatter, and \backmatter. In other classes you often find only the command \appendix, which is used to separate the body matter from the back matter — the assumption being that in articles and similar documents the front matter due to its length does not require special typographical treatment

## Front Matter Element
### Title Page

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=71&selection=109,0,143,1&color=yellow|p.I-26]]
> The standard LaTEX classes provide \title, \author (with \and and \thanks) and \date to set up the title information and \maketitle to produce the actual document title. For more elaborate title pages they offer the environment titlepage, which basically gives you an empty page in which you have to draw and position your title yourself.2


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=72&selection=4,1,32,0&color=yellow|p.I-27]]
> f you design your own title page, it might be worth taking a look at the collection Producing title pages of title page examples by Peter Wilson [199], which contains forty examples together with the (sometimes low-level) code to produce them. Another possibly helpful resource is the package titling by the same author, which provides methods for restyling the material produced by \title, \author, \thanks, \date, and \maketitle


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=72&selection=48,0,62,16&color=yellow|p.I-27]]
> A possible alternative is the little package authblk by Patrick Daly that provides Complex author information an extended syntax for the \author command and can typeset affiliation information either in blocks


![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=72&rect=66,105,500,363&color=yellow|p.I-27]]

### Content List

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=73&selection=6,0,29,9&color=yellow|p.I-28]]
> For the typical lists found in the front matter, such as the table of contents, Various content lists the standard classes support the commands \tableofcontents, \listoftables, and \listoffigures. Additional lists can be defined as explained in Section 2.3.4 on page 74. Typically such lists produce unnumbered headings. If your front matter requires further sectional units, such as a foreword or a preface, produce them with the star form of a suitable heading command, e.g., \chapter* or \section*

### Abstract

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=73&selection=31,0,55,7&color=yellow|Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition, p.I-28]]
> > Another important element, in particular for articles, is the abstract environAbstracts ment. Note that unfortunately the correct placement of this environment may depend on the chosen document class. In the standard classes and many others it is typeset where specified in the source, but there are classes in which it is formatted and placed by the \maketitle command and therefore has to appear before it. Its default formatting is usually adequate, and if you are typesetting an article for some particular journal, you should probably not alter it. However, if you do not like the outcome and you are free to make changes, take a look at the abstract package by Peter Wilson that offers a large arsenal of bells and whistles for adjusting most aspects of the abstract layout.

## Back Matter Element

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=73&selection=75,0,82,15&color=yellow|Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition, p.I-28]]
> > Probably the most often used back matter elements are a bibliography and an index, which are supported through the environments theindex and thebibliography
> 
> 

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=73&selection=85,0,98,33&color=yellow|Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition, p.I-28]]
> > If you have several other appendices, use heading commands of the appropriate level to introduce them. The numbering scheme for such headings is automatically adjusted by the \appendix or \backmatter declaration that separates the back matter material from the main text. However, if there is only a single appendix, it may look odd if that gets numbered. Thus, in that case, you may explicitly want to use the star form of the heading command.

## Slip into files

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=73&selection=102,0,114,8&color=yellow|Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition, p.I-28]]
> > LaTEX source documents can be conveniently split into several files by using \input or \include commands

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=73&color=yellow|p.I-28]]
> >  The \input command unconditionally includes the file specified as its argument at the current point. This is useful if you want to split your document into reasonably sized chunks or you want to reuse some parts for one or the other reason and therefore want to keep them in separate files

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=74&selection=8,0,35,4&color=yellow|p.I-29]]
> The \include command, however, is different in that it automatically starts a  new page before and after the included file. For each \include file a separate .aux file is produced, which is why in contrast to \input such files should be specified without extension and on the operating system level always have the extension .tex

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=74&selection=37,0,57,19&color=yellow|p.I-29]]
> The reason for \include is that documents can be reformatted piecewise by Partial processing specifying as arguments of an \includeonly declaration only those \include files LaTEX has to reprocess
> ![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=74&rect=76,355,371,462&color=yellow|p.I-29]]

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=74&selection=124,0,138,68&color=yellow|p.I-29]]
> Note that each document part loaded via \include starts on a new page and finishes by calling \clearpage; thus, floats contained therein do not move outside the pages produced by this part. Natural candidates for \include are therefore whole chapters of a book but not necessarily small fractions of text







