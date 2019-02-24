---
title: Continued Formatting
teaching: 00
exercises: 00

questions:
- "How do I perform more advanced formatting with LaTeX?"

objectives:
- "Learn how line breaking works in LaTeX"
- "Learn how LaTeX handles fonts and sizes"
- "Learn the most basic text formatting functions"
- "Break a body of text into sections"
- "Learn the justification commands"
- "Learn how to change text color"
- "Hyphenate custom words"
- "Use quotation marks the LaTeX way"
- "Use some symbols which have special character sequences"
- "Use non-qwerty characters"
- "Use the various dash signs"
- "Learn simple spacing commands"
- "Learn to enable/disable ligatures"

keypoints:
- "Separate a single paragraph into two with a double return"
- "Break lines manually using `\\`"
- "Change the typeface to `courier`"
- "Change text size with `Large`"
- "Format with `textbf`, `textit`, `underline`, `emph`"
- "Create Sections in a document with `section`"
- "Align some text to the right with `raggedright`"
- "Create hyphenation for new words with `hyphenation`"
- "Use ` and ' to create proper quotes"
- "Use `%` to display percentages"
- "Create a diacritic character such as `^o`"
- "Properly use an em and an en dash"
- "Force a nonbreaking space with `~`"

---

> In this episode we will learn the basic elements of LaTeX formatting options.
{: .callout}

## When and How Lines Break



## Typeface Controls



#### Relative Typeface Sizes

| Commands (smallest to Largest) |
|:------------------------------:|
|               tiny             |
|            scriptsize          |
|           footnotesize         |
|              small             |
|            normalsize          |
|              large             |
|              Large             |
|              LARGE             |
|               huge             |
|               Huge             |




## Text Formatting (weight, shape, etc.)


#### A Table of Common Text Formatting Options

| Command            | Result                   |
|:-------------------|:-------------------------|
| \textnormal{}      | document font (default)  |
| \emph{}            | emphasis                 |
| \textrm{}          | roman font               |
| \textsf{}          | sans serif font          |
| \texttt{}          | teletypefont (monospace) |
| \textup{}          | upright shape (default)  |
| \textit{}          | italic shape             |
| \textsl{}          | slanted shape            |
| \textsc{}          | Small Caps               |
| \uppercase{}       | ALL CAPS                 |
| \lowercase{}       | all lower case           |
| \textbf{}          | bold weight              |
| \textmd{}          | medium weight (default)  |
| \textlf{}          | light weight             |
| \textsubscript{}   | subscripted characters   |
| \textsuperscript{} | superscripted characters |


## Sections

Information is best displayed when well organized and in bite-sized parts.  For this reason, nearly
all documents are split into various sections.  A book has chapter, an article has sections, etc.
In LaTeX documents can be divided into multiple types of sections with different hierarchy levels.
The default configuration of LaTeX has several of these built in, and certain styles have even
more:

#### Section Levels

| Command          | Level |
|:-----------------|:-----:|
| \part{}          | -1    |
| \chapter{}       | 0     |
| \section{}       | 1     |
| \subsection{}    | 2     |
| \subsubsection{} | 3     |
| \paragraph{}     | 4     |
| \subparagraph{}  | 5     |

Each of these sections can have different formatting depending on the style sheet which has been
declared.  The sections are numbered, and automatically update the numbering information based on
the position when compiling.  The title of the section is entered into the curly braces of the
command, and all of the text below the command, until the section is changed, is formatted for
that particular section level.

> It is a [best practice]({{ page.root }}/reference/#best practice) to use tabs (four spaces) to
> denote text within sections.  That makes it easier for anyone reading the code to understand it.
> For example, the text starts out with no indents, then all text within the `document` environment
> is indented once.  All text within the first `section` is indented once more.  Text in a
> `subsection` is indented yet again.  And so on.
> ~~~
> \documentclass{article}
> \begin{document}
>   \section{Introduction}
>     Some introductory text.
>     \subsection{Specific Intro Information}
>       The specifics.
>   \section{Conclusion}
>     Concluding remarks.
> \end{document}
> ~~~
> {: .language-tex}
{: .callout}

Each time the document encounters a section, it will print the title of the section and the number.
However, in certain cases, sections should not be given numbers.  To prevent a section from
increasing the counter and printing the section number, an asterisk (`*`) is added to the command.

~~~
\documentclass{article}
\begin{document}
  \section{Some Section}
    Some text.
    \subsection{Count this section}
      Some text.
    \subsection*{But not this section}
      Some text.
    \subsection{And count this one}
      Some text.
\end{document}
~~~
{: .language-tex}

~~~
1. Some Section
  Some text.
1.a. Count this section
  Some text.
But not this section
  Some text.
1.b. And count this one
  Some text.
~~~
{: .output}

## Alignment


#### Alignment Options

| Command      | Result      |
|:-------------|:------------|
| \raggedleft  | align left  |
| \raggedright | align right |
| \centering   | centered    |


## Color

Color is not native to LaTeX, and must be handled by an external package.  There are several
options for packages which handle color, but we will be using `xcolor`.  This is a modernized
variant of the original `color` package.


## Custom Dictionaries




## Quotation Marks




## Fancy Characters with Escaped Sequences


#### Table of Special Characters

|       Command       | Character |
|:--------------------|:---------:|
| \%                  |   `%`     |
| \$                  |   `$`     |
| \{                  |   `{`     |
| \_                  |   `_`     |
| \P                  |   `¶`     |
| \ddag               |   `‡`     |
| \textbar            |   `|`     |
| \textgreater        |   `>`     |
| \textendash         |   `–`     |
| \texttrademark      |   `™`     |
| \textexclamdown     |   `¡`     |
| \textsuperscript{a} |  `X^a`    |
| \pounds             |   `£`     |
| \#                  |   `#`     |
| \&                  |   `&`     |
| \}                  |   `}`     |
| \S                  |   `§`     |
| \dag                |   `†`     |
| \textbackslash      |   `\`     |
| \textless           |   `<`     |
| \textemdash         |   `—`     |
| \textregistered     |   `®`     |
| \textquestiondown   |   `¿`     |
| \textcircled{a}     |   `ⓐ`     |
| \copyright          |   `©`     |
| \ldots              |  `. . .`  |


\usepackage[gen]{eurosym}

## Accented Letters


#### Table of Accented Characters

| Command | Sample | Description                              |
|---------|:------:|------------------------------------------|
| \\`{o}  |   `ò`  | grave accent                             |
| \'{o}   |   `ó`  | acute accent                             |
| \^{o}   |   `ô`  | circumflex                               |
| \"{o}   |   `ö`  | umlaut, trema or dieresis                |
| \H{o}   |   `ő`  | long Hungarian umlaut (double acute)     |
| \~{o}   |   `õ`  | tilde                                    |
| \c{c}   |   `ç`  | cedilla                                  |
| \k{a}   |   `ą`  | ogonek                                   |
| \l{}    |   `ł`  | barred l (l with stroke)                 |
| \={o}   |   `ō`  | macron accent (a bar over the letter)    |
| \b{o}   |   `o`  | bar under the letter                     |
| \.{o}   |   `ȯ`  | dot over the letter                      |
| \d{u}   |   `ụ`  | dot under the letter                     |
| \r{a}   |   `å`  | ring over the letter                     |
| \u{o}   |   `ŏ`  | breve over the letter                    |
| \v{s}   |   `š`  | caron/háček ("v") over the letter        |
| \t{oo}  |  `o͡o`  | "tie" (inverted u) over the two letters  |
| \o      |   `ø`  | slashed o (o with stroke)                |


## Hyphenation Differentiation



#### Table of Dashes

| Input | Output | Purpose     |
|:------|:------:|:------------|
| -     |    -   | inter-word  |
| --    |    –   | page range  |
| ---   |    —   | punctuation |
| $-$   |    −   | minus sign  |

## Controlling Space

\\

~




















{% include links.md %}
