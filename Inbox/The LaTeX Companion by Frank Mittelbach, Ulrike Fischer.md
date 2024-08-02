---
tags:
  - 工具/Tex
  - 工具/LaTex
  - year/2024
date: 2024-07-02 17:35:32
---
[[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf]]
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

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=75&selection=6,0,32,13&color=yellow|Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition, p.I-30]]
> > It is very important to note that some packages can not be used reliably with the \include mechanism. Likely candidates are those that write their own support files to store data between runs as they often do not realize that parts of the document are not processed. A premier example from this book is the acro package. It always considers the first acronym it sees as being the acronym that is showing the full form; thus, if you apply \includeonly, it may see different instances as being the first, thereby altering the line breaking and pagination compared to always processing the full document
> 
> 


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=75&selection=110,0,119,41&color=yellow|p.I-30]]
> Sometimes it is useful to keep several versions of a document together in a single source, especially if most of the text is shared between versions. This functionality is provided by the tagging package1 created by Brent Longborough (1944–2021).
> 
> ![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=75&rect=107,195,444,226&color=yellow|p.I-30]]
> 
> ![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=76&rect=63,364,506,493&color=yellow|p.I-31]]
> 
> ![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=76&rect=68,215,491,294&color=yellow|p.I-31]]

## section command

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=77&selection=116,0,153,59&color=yellow|p.I-32]]
> Standard LaTEX provides the set of sectioning commands1 shown in Table 2.1. The \chapter command defines level zero of the hierarchical structure of a document, \section defines level one, and so on, whereas the optional \part command defines the level minus one (or zero in classes that do not define \chapter). Not all of these commands are defined in all document classes. The article class does not have \chapter, and the letter class does not support sectioning commands at all. It is also possible for a package to define other sectioning commands, allowing either additional levels or variants for already supported levels.
> 
> ![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=77&rect=95,509,480,613&color=yellow|p.I-32]]


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=78&selection=86,0,103,32&color=yellow|p.I-33]]
> The first form performs all of the above actions. If the optional argument toc-entry is present, it is used as the text string for the table of content and the running header and/or footer; otherwise, the title is also used for those places. In particular this means that you cannot specify different texts for the table of content and for the running header through this interface. The numbering depends on the current value of the counter secnumdepth (discussed in the next section).
> 
> ![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=78&rect=58,519,314,551&color=yellow|p.I-33]]

## Section Numbering

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=79&selection=8,0,13,34&color=yellow|p.I-34]]
> To support numbering, LaTEX uses a counter for each sectional unit and composes the heading number from these counters

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=79&selection=14,0,41,74&color=yellow|p.I-34]]
> Perhaps the change desired most often concerning the numbering of titles is to alter the nesting level up to which a number should be produced. This is controlled by a counter named secnumdepth, which holds the highest level with numbered headings. For example, some documents have none of their headings numbered. Instead of always using the starred form of the sectioning commands, it is more convenient to set the counter secnumdepth to -2 in the document preamble. The advantages of this method are that an entry in the table of contents can still be produced and that arguments from the sectioning commands can produce information in running headings. As discussed, these features are suppressed in the starred form.


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=79&selection=42,0,57,22&color=yellow|p.I-34]]
> To number all headings down to \subparagraph or whatever the deepest sectioning level for the given class is called, setting the counter to a high enough value (e.g., a declaration such as \setcounter{secnumdepth}{5} would be sufficient for the standard classes).

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=79&selection=58,0,80,35&color=yellow|p.I-34]]
> Finally, the \addtocounter command provides an easy way of numbering more or fewer heading levels without worrying about the level numbers of the corresponding sectioning commands. For example, if you need one more level with numbers, you can place \addtocounter{secnumdepth}{1} in the preamble of your document without having to look up the right value. In some cases this might even be useful within the document; see also the package tocvsec2 by Peter Wilson that provides further support for such occasions.


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=79&selection=135,0,136,79&color=yellow|p.I-34]]
> Normally, when a counter at a given hierarchical level is incremented, then the next lower-level counter (i.e., that with the next higher-level number) is rese
> 
> ![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=79&rect=125,97,411,185&color=yellow|p.I-34]]
> 


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=80&selection=64,0,75,50&color=yellow|p.I-35]]
> Every counter in LaTEX, including the sectioning counters, has an associated command constructed by prefixing the counter name with \the, which generates a typeset representation of the counter in question. In the case of the sectioning commands, this representation form is used to produce the full number associated with the commands, as in the following definitions:
>```
>\renewcommand\thechapter{\arabic{chapter}} \renewcommand\thesection{\thechapter.\arabic{section}} \renewcommand\thesubsection{\thesection.\arabic{subsection}}
>```


![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=81&rect=29,444,452,533&color=yellow|p.I-36]]
> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=81&selection=40,1,77,58&color=yellow|p.I-36]]
> n other words, the counter representation commands are also used by LaTEX’s cross-referencing mechanism (the \label and \ref commands; see Section 2.4). Therefore, we can make only small changes to the counter representation commands so that their use in the \ref command still makes sense. To produce the box around the heading number without spoiling the output of a \ref, we would have to redefine LaTEX’s internal command \@seccntformat, which is responsible for typesetting the counter part of a section title. As this is rather messy, it is better to use the interface provided by the titlesec package for this, which is what we do in the next example.

![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=81&rect=28,260,439,347&color=yellow|p.I-36]]


## changing fixed heading texts

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=81&selection=132,0,132,60&color=yellow|p.I-36]]
> Some of the standard heading commands produce predefined text
> 
> ![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=82&rect=69,498,438,611&color=yellow|p.I-37]]
> 
> ![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=82&rect=69,302,475,376&color=yellow|p.I-37]]
> 

## Heading Design

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=82&selection=127,0,128,4&color=yellow|p.I-37]]
> Headings can be loosely subdivided into two major groups: display and run-in headings

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=82&selection=128,6,129,61&color=yellow|p.I-37]]
> A display heading is separated by a vertical space from the preceding and the following text — most headings in this book are of this type.

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=82&selection=130,0,138,42&color=yellow|p.I-37]]
> A run-in heading is characterized by a vertical separation from the preceding text, but the text following the title continues on the same line as the heading itself, only separated from the latter by a horizontal space. In many classes the lower-level headings such as \paragraph are formatted as run-in headings. Note that an empty line after the heading command is ignored.
> ![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=82&rect=66,62,481,140&color=yellow|p.I-37]]


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=83&selection=10,0,21,26&color=yellow|p.I-38]]
> We then discuss all other design aspects that are supported through the high-level interfaces of the titlesec package. At the very end we also briefly look at the low-level support offered by LaTEX because this is helpful in understanding the code found in older document class files.

### quotchap packages

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=83&selection=32,0,41,88&color=yellow|p.I-38]]
> An interesting way to enhance \chapter headings is provided by the quotchap package created by Karsten Tinnefeld with later updates by Jan Klever. It allows the user to specify quotation(s) that will appear on the top left of the chapter title area.

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=83&selection=42,0,50,0&color=yellow|p.I-38]]
> The quotation(s) for the next chapter are specified in a savequote environment; the width of the quotation area can be given as an optional argument defaulting to 10cm

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=83&selection=50,2,54,28&color=yellow|p.I-38]]
> Each quotation should finish with a \qauthor command to denote its source

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=83&selection=56,0,71,12&color=yellow|p.I-38]]
> The default layout produced by the package can be described as follows: the quotations are typeset in \slshape, placed flush left, followed by vertical material stored in the command \chapterheadstartvskip. It is followed by a very large chapter number, typeset flush right in 60% gray, followed by the chapter title text, also typeset flush right. After a further vertical separation, taken from the command \chapterheadendvskip, the first paragraph of the chapter is started without indentation.

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=83&selection=72,0,77,9&color=yellow|p.I-38]]
> The number can be printed in black by specifying the option nogrey to the package. 

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=83&selection=86,57,90,11&color=yellow|p.I-38]]
>  Alternatively, you can explicitly specify a font family (basically any of those listed in the tables in Chapter 10) as an argument to \qsetcnfont

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=83&selection=91,2,96,15&color=yellow|p.I-38]]
> Or you could redefine the \chapnumfont command, which is ultimately responsible for selecting the font and font size for the chapter number.

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=83&selection=97,0,116,32&color=yellow|p.I-38]]
> The \quotefont command defines the font used for the quote, and with the help of \qauthorfont you can alter the font for the author name (which is why we still get a sans serif font in the example even though only \scshape was specified). Finally, the font for the chapter title font can be influenced by redefining the \sectfont command as shown in the example.

![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=84&rect=47,424,503,615&color=yellow|p.I-39]]

### epigraph packages

![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=84&rect=47,123,507,302&color=yellow|p.I-39]]

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=84&color=yellow|p.I-39]]
> Standard LaTEX document classes and many others, following (American) English typographic tradition, suppress the indentation of the first paragraph after a display heading. While this can be changed with an option to titlesec (see below), it can also be done through the little1 package indentfirst by David Carlisle, regardless of whether or not the titlesec package is loaded.

### nonumonpart packages

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=85&selection=31,0,58,34&color=yellow|p.I-40]]
> Another often asked for adjustment is to drop page numbers on part titles. On chapter headings this can be easily manually achieved using \thispagestyle{empty}, but because \parts in many classes occupy a whole page, there is no possibility to place such a declaration.2 To solve this without any manual work someone suggested a few lines of code, and Yvon Henel took the effort to put them into the little nonumonpart package. It works for the standard classes report and book and any other class that is derived from them. All you have to do is load the package; there are no options or other customization possibilities.

### titlesec packages

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=85&selection=66,0,75,1&color=yellow|p.I-40]]
> The titlesec package created by Javier Bezos provides a flexible and fairly comprehensive reimplementation of the basic heading tools offered by Standard LaTEX

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=85&selection=77,75,86,7&color=yellow|p.I-40]]
> notable exceptions are memoir and the KOMA-Script classes

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=85&selection=93,57,95,78&color=yellow|p.I-40]]
> The package supports two interfaces: a simple one for smaller adjustments, which is realized mainly by options to the package, and an extended interface to make more elaborate modifications.

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=85&selection=99,0,159,14&color=yellow|p.I-40]]
> The basic interface lets you modify the font characteristics of all headings by specifying one or more options to set a font family (rm, sf, tt), a font series (md, bf), or a font shape (up, it, sl, sc). The title size can be influenced by selecting one of the following options: big (same sizes as for standard LaTEX classes), tiny (all headings except for chapters in text size), medium, or small, which are layouts between the two extremes. The alignment is controlled by raggedleft, center, or raggedright, while the vertical spacing can be reduced by specifying the option compact as shown later

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=85&selection=160,0,168,32&color=yellow|p.I-40]]
> To modify the format of the number accompanying a heading, the command \titlelabel is available. Within it \thetitle refers to the current sectioning

![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=86&rect=66,481,509,575&color=yellow|p.I-41]]
#### title format
```
\title format*{cmd}{format}
```

![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=86&rect=68,237,497,332&color=yellow|p.I-41]]


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=87&selection=40,0,42,9&color=yellow|p.I-42]]
> Interpretation of heading command arguments

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=87&selection=65,0,67,0&color=yellow|p.I-42]]
> Indentation after heading

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=87&selection=79,0,80,5&color=yellow|p.I-42]]
> Adjusting “empty” pages

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=87&selection=104,0,106,10&color=yellow|p.I-42]]
> \part* in the TOC

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=87&selection=127,0,131,0&color=yellow|p.I-42]]
> Fixing a TOC problem with \part

#### extended interface

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=87&selection=146,0,156,21&color=yellow|p.I-42]]
> The extended interface consists of two major commands, \titleformat and \titlespacing. They allow you to declare the “inner” format (i.e., fonts, label, alignment, . . . ) and the “outer” format (i.e., spacing, indentation, etc.), respectively. This scheme was adopted because people often wish to alter only one or the other aspect of the layout.

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=88&selection=4,0,18,1&color=yellow|p.I-43]]
> ```
\titleformat{cmd}[shape]{format}{label}{sep}{before-code}[after-code]


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=88&selection=38,0,127,2&color=yellow|p.I-43]]
> shape The basic shape for the heading. A number of predefined shapes are available: hang, the default, produces a hanging label (like \section in standard classes); display puts label and heading text on separate lines (like standard \chapter); while runin produces a run-in title (like standard \paragraph). In addition, the following shapes, which have no equivalents in standard LaTEX, are provided: frame is similar to display but frames the title; leftmargin puts the title into the left margin, while rightmargin places it into the right margin. The last two shapes might conflict with \marginpar commands; that is, they may overlap. A general-purpose shape is block, which typesets the heading as a single block. It should be preferred to hang for centered layouts. Both drop and wrap wrap the first paragraph around the title, with drop using a fixed width for the title and wrap using the width of the widest title line (automatically breaking the title within the limit forced by the left-sep argument of \titlespacing).

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=88&selection=129,0,129,6&color=yellow|p.I-43]]
> format
> 
> > ([[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=88&selection=132,36,141,9&color=yellow|p.I-43]])
> which is typeset following the space above the heading. If you need horizontal material, it should be entered in the label or before-code argument.


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=88&selection=143,0,144,0&color=yellow|p.I-43]]
> label
> > ([[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=88&selection=145,0,145,56&color=yellow|p.I-43]])
> The formatting of the label, that is, the heading number


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=88&selection=167,0,169,76&color=yellow|p.I-43]]
> sep 
> Length whose value determines the distance between the label and title text.


> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=88&selection=182,0,184,52&color=yellow|p.I-43]]
> before-code 
> Code executed immediately preceding the heading text

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=88&selection=206,0,208,61&color=yellow|p.I-43]]
> after-code 
> 
> Optional code to be executed after formatting the heading tex

![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=89&rect=31,424,467,513&color=yellow|p.I-44]]

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=89&selection=76,0,86,1&color=yellow|p.I-44]]
> ```
   \titlespacing*{cmd}{left-sep}{before-sep}{after-sep}[right-sep]

> [!PDF|yellow] [[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=89&selection=104,0,165,1&color=yellow|p.I-44]]
> left-sep 
> Length specifying the increase of the left margin for headings with the block, display, hang, or frame shape. With ...margin or drop shapes it specifies the width of the heading title, with wrap it specifies the maximum width for the title, and with runin it specifies the indentation before the title (negative values would make the title hang into the left margin). 
> 
> before-sep 
> Length specifying the vertical space added above the heading. 
> 
> after-sep
>  Length specifying the separation between the heading and the following paragraph. It can be a vertical or horizontal space depending on the shape deployed. 
>  
>  right-sep 
>  Optional length specifying an increase of the right margin, which is supported for the shapes block, display, hang, and frame.


![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=90&rect=58,492,520,579&color=yellow|p.I-45]]

![[Frank Mittelbach, Ulrike Fischer - The LaTeX Companion_ Parts I & II, 3rd Edition.pdf#page=90&rect=59,314,509,430&color=yellow|p.I-45]]
