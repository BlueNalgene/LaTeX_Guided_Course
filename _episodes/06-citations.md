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
contents, tables, and figures we are using elsewhere in the document.  LaTeX allows us easily perform
both indexing and cross-referencing.

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
the BibTeX format.  The format stores information about the title, author, year, url, and other
relevant information for publications you intend to cite.  Each BibTeX entry is given a type,
such as journal article, web-page, report, etc., and a unique identifier.  When information is
cited in the LaTeX document by referencing the identifier, LaTeX and BibTeX parse the file for
the type of each entry.  Then, based on the settings in the LaTeX document, BibTeX prints the
relevant information.  This means that BibTeX entries can store information that may not be used
within the document.

The BibTeX format is very common in academic circles.  When an academic paper is accessed from a
database online, there is often an option to "export" the citation.  If you are using a citation
manager (which is highly recommended), you might already be familar with exporting meta files.

Citation managers including Zotero, Mendeley, and EndNote, support exporting libraries as BibTeX
files.  This makes it particularly easy to collect references you intend to use in a file, and
have it ready to go when preparing a document.

### Inline Citation

To cite works within the text of your document, use the `cite` command with the unique identifier
of the BibTeX entry you want.  This operates similarly to the `ref` command by putting the
inline citation exactly where you declare it.  The proper way to format this in your text such that
the page rendering does not automatically wrap the citation around to a new line is to use a
non-breaking space (`~`) before each citation command.

~~~
This is some text blah blah.~\cite{2008Einstein}
~~~
{: .language-tex}

Multiple citations can be placed in a single `cite` command.  Each identifier you want to cite
should be separated by a comma (`,`).

~~~
This is some text blah blah.~\cite{2008Einstein, 2009Lamport, 2001Gonzales}
~~~
{: .language-tex}

Adding an options to the `cite` command enclosed in square braces will add text to the inline
citation.  This is useful for including page or chapter information.  Simply place the page
number or range of numbers in the brackets to automatically produce the necessary modification.

~~~
This is some text blah blah.~\cite[84]{2008Einstein}
~~~
{: .language-tex}

### Footnote Citation

Certain publication formats will require citations to be placed in the footnotes of the page the
inline citation occurs on.  LaTeX does not support this natively, so we need to pull in a package
which can handle it called `footbib`.  The `cite` command is replaced by `footcite`, and has many
of the same rules as `cite`.

~~~
This is some text blah blah.~\footcite{2008Einstein}
~~~
{: .language-tex}

### Creating a Bibliography

Of course, if inline citations are used, there must be a bibliography or works cited section to
contain the references.  We first declare how the bibliography should look using
`bibliographystyle`.  There are several default options available:

|  Style  | Description                                                           |
|:-------:|:----------------------------------------------------------------------|
|  abbrv  | Abbreviated first name, full last name.  Ordered based on appearance  |
|   acm   | Association of Computing Machinery style                              |
|  alpha  | Alphanumeric inline reference values, not numbered                    |
| apalike | APA Like citation style                                               |
|  ieeetr | IEEE Transactions Style                                               |
|  plain  | The default style.  Lists everything                                  |
|  siam   | Society for Industrial and Applied Mathematics style                  |
|  unsrt  | Sorts references based on order in `.bib` file, not in paper          |

On the next line, the command `bibliography` is issued with curly braces holding the filenames
of your BibTeX file.  The filetype (`.bib`) is **NOT** added.  If the BibTeX file is not in same
the root directory as your LaTeX file, then you must declare the full path.  However, it is
recommended to include a unique BibTeX file in the root project directory for each document you
create to aid portability.

~~~
\bibliographystyle{plain}
\bibliography{bibfile}
~~~
{: .language-tex}

There are many more styles of inline and reference citations available outside of the default
LaTeX configuration.  Some document classes provided by publishers will require certain custom
bibliography styles to be used.  For these, it is important to read the documentation for to match
the requirements of the class.  The `natbib` package is commonly used to provide more options for
formatting citations.  It operates very similarly to the default BibTeX use we have learned here.
Consult the documentation for more information.









{% include links.md %}
