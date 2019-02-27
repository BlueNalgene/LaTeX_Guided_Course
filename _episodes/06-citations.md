---
title: Cross-referencing, Citations, and BibTeX
teaching: 00
exercises: 00

questions:
- "How do I cite my sources in LaTeX?"

objectives:
- "Create a Table of Contents"
- "Create a List of Figures"
- "Create a List of Tables"
- "Create an Appendix"
- "Cross-reference within your text"
- "Explain BibTeX"
- "Import a BibTeX file into a document"
- "Create a bibliography"
- "Cite an article in-line"
- "Cite as a footnote"
- "Change the way citations are represented in the bibliography and in the text"


keypoints:
- "Create a Table of Contents with `tableofcontents`"
- "Create a List of Figures with `lisfoffigures`"
- "Create a List of Tables with `listoftables`"
- "Prevent a section from being counted using `*`"
- "Change how deep sections are counted using `setcounter{tocdepth}`"
- "Declare a region of sections to be numbered as Appendices with `appendix`"
- "Reference a figure number in text by labeling it with `label` and calling it with `ref`"
- "Create a BibTeX entry manually with `bibitem` within `thebibliography` environment"
- "Create a bibliography in the text with `bibliography` and `bibliographystyle`"
- "Import a premade `.bib` file with `bibliography`"
- "Create an inline citation number with `cite`"
- "Place a citation in a footnote using `footnote{cite{}}`"
- "Change they way the citation appears with `natbib`"



---

When constructing a large document such as a book or a thesis, we must often reference the
contents, tables, and figures we are using elsewhere in the document.  We can easily perform
both indexing and cross-referencing in LaTeX.

## Indexing

The indexing covered here will include the simple methods by which lists of content can be added
to a document.  While it is possible to create detailed indexes, such as one would find in the back
of a textbook, that will not be covered here.

### Table of Contents, List of Figures, List of Tables

All `section`, `subsection`, and similar hierarchal headings are numbered automatically by LaTeX.
A list of these contents can be generated using a table of contents by issuing the
`tableofcontents` command.  The table will generate with the name of each section heading and a
corresponding page number.

Similarly, a list of the figures and tables used in the document can be generated using
`listoffigures` and `listoftables`, respectively.  Each add a reference to the automatically
generated figure or table number, and include a page number for reference.

It is worth nothing that any `section*`, `figure*`, `table*`, or other environment starred (`*`)
to prevent increasing the counter will not appear on these indexes, nor will the numbering of items
in the index increase, showing a gap where a starred item is.

It is possible to change the numbering of index items manually.  This is useful in cases such as
telling LaTeX to interpret a "preface" type section as the 0th section or jumping values to work on
a certain "chapter".  These can be modified using the `setcounter` command.  The `setcounter`
command takes two arguments in separate curly braces.  The first argument is the type of object you
want to change the number of (e.g. `subsection`, `figure`, or `table`), and the second argument is
the value you want to set it at.  For example, if you issue `\setcounter{table}{3}`, the next table
will be Table 4.

It is possible to ignore certain sub- levels in an index with `setcounter`.  By issuing the first
argument as `tocdepth` and the second argument `5`, the table of content will show
sub-sub-sub-sub-section level content with page numbers (this type of section is called `paragraph`
when issuing sectioning commands).


### Appendices

It is possible to create sections with a unique numbering scheme.  There are some advanced uses of
this we will not cover here, but there is a notable common use.  When an `appendix` command is
issued once, LaTeX will treat every section added below that line as an Appendix.  Depending on the
`documentclass` you are using, appendices may be ignored altogether or be numbered in a unique way
such as "A1, A2, etc.

### Abstracts

Research documents and many other academic publications will require the use of an abstract.  The
`abstract` environment will alter the formatting of the content contained within it to match the
style of the `documentclass`, but it will not be added to any indexes.  Often, there are unique
requirements for issuing the `abstract` command in a `documentclass` supplied by an academic
publisher.  Remember to read all of the documentation so that your paper meets the content
guidelines.

## Cross Referenes

Cross-referencing within the text of a document is used to tell the audience which table, figure,
or section you are referencing.  Since LaTeX issues the numbers of these environments dynamically,
we need to label them in a meaningful way.  Inside each environment you may reference, usually on
the first line of that environment, a `label` command can be issued with some unique identifier
within the curly braces.  While the unique identifier can be anything you choose, there is a
standard convention to include a type before the identifier, making a label for some arbitrary
figure read: `\label{fig:arbitrary}`.  A list of the standardized label types are:

|   Code    |     Meaning     |   Code    |     Meaning     |
|:---------:|:----------------|:---------:|:----------------|
| `ch:`     | chapter         | `fig:`    | figure          |
| `sec:`    | section         | `tab:`    | table           |
| `subsec:` | subsection      | `eq:`     | equation        |
| `lst:`    | code listing    | `itm:`    | list item       |

These standards are useful for reading the LaTeX code when you have forgotten the exact meaning,
and for keeping anyone reviewing your work informed.  We all know how important it is to keep
reviewers happy!

To reference something you have labeled in the text, simply use the `ref` command with your
identifier.  This will place a reference exactly where you tell it in the body of the text to
whatever dynamically numbered thing you are referencing.

There are techniques to label and reference portions of your document in more advanced ways,
such as labeling of individual steps in a multiline equation, but that is considered an advanced
topic.

## Citations and Bibliographies


### BibTeX Files

Information for LaTeX works cited in the paper is stored in a special file (`.bib` filetype) in
the BibTeX format.

### Inline Citation


### Footnote Citation


### Creating a Bibliography











{% include links.md %}
