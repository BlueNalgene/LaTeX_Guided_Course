---
title: LaTeX Lists and Tables
teaching: 00
exercises: 00

questions:
- "How do I add a table to my document?"

objectives:
- "Learn how to make an itemized list"
- "Learn how to make an enumerated list"
- "Learn how to make a descriptive list"
- "Know how tables are arranged in LaTeX"
- "Create a simple table"
- "Be able to justify cells of a table"
- "Deal with linebreaking within cells"
- "Use line barriers to make a table easier to read"
- "Make tables with multi-row or column stretches"
- "Adjust sizes, spacing, and placement of a table"

keypoints:
- "Convert text to a bulleted list with `itemize`"
- "Convert sequential to a numbered list with `enumerate`"
- "Define terms with a `description` list"
- "Create a basic table with `tabular`"
- "Justify cells with `l`, `c`, and `r`"
- "Position text within cells vertically with `t`, `c`, and `b`"
- "Use `p` to wrap lines of text within a cell"
- "Create vertical barriers between columns with `|`"
- "Create horizontal barriers between rows with `hline`"
- "Use `multicolumn` and `multirow` to make joined cells"
- "Adjust the size scale of a table using `resizebox`"
- "Influence page position with float positioning arguments `h`, `t`, `b`, and `p`"

---


		\begin{itemize}
			\item[\meow] My cat's name is Leon
			\item[\meow] He is a handsome little man
			\item[\meow] Also a jerk
		\end{itemize}

## Itemized Content


### Itemized Lists


### Enumerated Lists


### Descriptive Lists


## LaTeX Tables


### Another Row? Another Line Break!


### Ampersand Separation


> It is a [best practice]({{ page.root }}/reference/#best practice) to organize your columns in
> your LaTeX file by the size of their content.  This will make it easier for you to read and make
> edits.  Most editors should use a monospace font, making this easy to implement.

### Row Alignment


### Horizontal and Vertical Separators


### Stretching or Merging Cells


## Float the Table
