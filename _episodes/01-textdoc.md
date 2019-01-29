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

When creating a document in a [WYSIWYG]() editor, we tend to think of the document as a whole.  We
think as writers.  Each portion of the document is a jumble that must be perfected as it is
written.

When a document is created in [LaTeX](), we must command like programmers.  Each portion of the
document may be constructed independent of content or context.  Commands are given which will
perform the same function upon each compile.  Just as we command like programmers, we must learn
to think as *programs*.  Each portion of the LaTeX [markdown language]() must follow order that can
be interpreted by the compiler and have logical flow.

For this reason, we organize our document into parts which compromise making sense to the compiler
and the operator.  In the most general sense, we divide a [.tex]() document into [preamble](), and
content sections.  The preamble is where we tell the compiler everything it needs to know to be
able to process the content within.

We distinguish these sections by restricting them to an [environment]().  For example, the content
of a document will be entirely contained within an environement we call `document`.  An environment
must have a beginning and an end, making it look like:

~~~
\begin{document}
  our document's contents
\end{document}
~~~
{: .language-tex}



This is great but not very interesting.
To do anything useful with data, we need to assign its value to a _variable_.
In Python, we can [assign]({{ page.root }}/reference/#assign) a value to a
[variable]({{ page.root }}/reference/#variable), using the equals sign `=`.
For example, to assign value `60` to a variable `weight_kg`, we would execute:


~~~
weight_kg_text = 'weight in kilograms:'
~~~
{: .language-tex}


~~~
\begin{document}

\maketitle

blah

\end{document}
~~~
{: .language-tex}
