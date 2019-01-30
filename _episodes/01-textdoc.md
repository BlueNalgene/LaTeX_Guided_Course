---
title: Simple Text Document
teaching: 00
exercises: 00

questions:
- "How do I start a LaTeX document?"

objectives:
- "Explain the sections of a LaTeX document"
- "Understand how LaTeX distinguishes text from command"
- "Learn about commenting your code"
- "Create a preamble which generates a simple document"
- "Create title section"
- "Perform simple tasks using both functions and environments"
- "Change the document class"
- "Use a nonstandard document class"
- "Break a body of text into sections"
- "Learn about what a package is and how to import one"
- "Learn where to read more about libraries"
- "Use custom library functions"
- "Compile a document for the first time and save the PDF."

keypoints:
- "Comment text with `%`"
- "Create a simple document with `documentclass`"
- "Distinguish preamble from `begin{document}` ... `end{document}`"
- "Use a `maketitle` section."
- "Use various document classes such as `article`, `report`, and `beamer`"
- "Import a custom `.cls` file"
- "Create Sections in a document with `section`"
- "Use the non-standard library `import{textcase}'"
- "Use a command from an imported library 'MakeTextUppercase'"
- "Export a compiled document as a PDF"

---

In this episode we will learn the essential structure of a document produced in LaTeX, and we will
begin to create our first document.

## Document Organization

When creating a document in a [WYSIWYG]({{ page.root }}/reference/#WYSIWYG) editor, we tend to
think of the document as a whole.  We think as writers.  Each portion of the document is a jumble
that must be perfected as it is written.

When a document is created in [LaTeX]({{ page.root }}/reference/#LaTeX), we must command like
programmers.  Each portion of the document may be constructed independent of content or context.
Commands are given which will perform the same function upon each compile.  Just as we command
like programmers, we must learn to think as *programs*.  Each portion of the LaTeX
[markdown language]({{ page.root }}/reference/#markdown language) must follow order that can be
interpreted by the compiler and have logical flow.

For this reason, we organize our document into parts which compromise making sense to the compiler
and the operator.  In the most general sense, we divide a [.tex]({{ page.root }}/reference/#.tex)
document into [preamble]({{ page.root }}/reference/#preamble), and content sections.  The preamble
is where we tell the compiler everything it needs to know to be able to process the content within.

We distinguish these sections by restricting them to an
[environment]({{ page.root }}/reference/#environment).  For example, the content of a document will
be entirely contained within an environement we call `document`.  An environment must have a
beginning and an end, making it look like:

~~~
\begin{document}
  our document's contents
\end{document}
~~~
{: .language-tex}

The minimum acceptable document in LaTeX must include declaring the `documentclass`, then using a
`document` environment.

~~~
\documentclass{minimal}

\begin{document}
  The simplest document
\end{document}
~~~
{: .language-tex}

The `documentclass` tells the LaTeX interpreter program what style to apply to our output. There
are many different document classes aside from `minimal` which we will discuss later, but for now,
we will confine all of our experiments and learning in this format.

The code is organized such that all of the declarations about *how* LaTeX should form the document,
including `documentclass` are placed in the preamble.  Everything else must be bound by the
`document` environment.

## Commands and Environments

The entirety of "our document's contents" is bound by commands.  We can tell that these are
commands in LaTeX, commands are declared with the backslash (`\`).  An environment will `begin` and
`end` at the boundaries declared.  So if we want to use a [math mode]({{ page.root }}/reference/#math mode)
environment (something which will be discussed later in this lesson) with an equation we would use:

~~~
\begin{document}
  \begin{equation}
    our equation
  \end{equation}
\end{document}
~~~
{: .language-tex}

Some commands in LaTeX are not treated as environments.  These direct commands are also called
using the backslash (`\`), but they do not have be told where to begin and end.  A command executes
only once each time it is called.  Within the math mode environment above, we will execute a
command to insert the special character for the lowercase Greek letter, sigma (σ).

~~~
\begin{document}
  \begin{equation}
    \sigma
  \end{equation}
\end{document}
~~~
{: .language-tex}
~~~
σ
~~~
{: .output}

Commands can have one or more [argument]({{ page.root }}/reference/#argument) when it is called.
An argument modifies the command in some manner.  In LaTeX, optional arguments are declared using
braces (`[` and `]`).  Main arguments are declared within curly braces (`{` and `}`).  If a command
is called without using these characters, LaTeX will assume you included a set of empty curly
braces.  Thus,

~~~
\command
~~~
{: .language-tex}

defaults to

~~~
\command{}
~~~
{: .language-tex}

Since the command `\sigma` used above does not *require* an argument, it is accepted by the
compiler.  Some commands require one or more argument to function.  In this case, the compilation
would fail and give an error.  It is important to know what each command requires when you use it.

## Special Characters

LaTeX reads each character written in the code and interprets it based on the context.  Certain
characters such as the back slash `\`, as we have seen, have special properties.  But what if we
wish to use a character in our document that has been assigned as a special character?  In this
case, we must tell LaTeX to treat the character like text.  For this purpose, LaTeX provides
[escape sequences]({{ page.root }}/reference/#escape sequence) which print the character.  These
escape sequences operate similar to commands.  So if we wish to include a back slash in our text,
we use the command `\textbackslash`:

~~~
\textbackslash
~~~
{: .language-tex}
~~~
\
~~~
{: .output}

Most special characters are escaped with a backslash and the symbol, but others require a command
phrase.  The correct command phrase may be esoteric to a novice LaTeX user, and difficult to
remember.  There are many sources available on the internet which can assist with finding the
'magic word'.  The following characters have special meaning within LaTeX, and require escape
sequences:

~~~
\& \% \$ \# \_ \{ \} \textasciitilde \textasciicircum \textbackslash
~~~
{: .language-tex}

~~~
& % $ # _ { } ~ ^ \
~~~
{: .output}

Each of these symbols, un-escaped, affect the compilation of the LaTeX code.  For example, use of
the percent sign (`%`) tells LaTeX to treat the rest of the line as a
[comment]({{ page.root }}/reference/#comment).  Comments allow the user to hide text such as notes
to other authors or unused code from the compiler, such that it does not appear on the final
document.

~~~
Print this text but not
%this text
comments
~~~
{: .language-tex}

~~~
Print this text but not
comments
~~~
{: .output}

