---
title: Continued Formatting
teaching: 00
exercises: 00
questions:
- "How do I perform more advanced formatting with LaTeX?"

objectives:
- "Learn how LaTeX handles fonts and sizes"
- "Learn the most basic text formatting functions"
- "Learn the justification commands"
- "Learn how line breaking works in LaTeX"
- "Learn how to change text color"
- "Hyphenate custom words"
- "Use quotation marks the LaTeX way"
- "Use some symbols which have special character sequences"
- "Use non-qwerty characters"
- "Use the various dash signs"
- "Learn simple spacing commands"
- "Learn to enable/disable ligatures"


keypoints:
- "Change the typeface to `courier`"
- "Change text size with `\Large`"
- "Format with `\textbf`, `\textit`, `\underline`, `\emph`"


---


Command	Output
\tiny	sample text
\scriptsize	sample text
\footnotesize	sample text
\small	sample text
\normalsize	sample text
\large	sample text
\Large	sample text
\LARGE	sample text
\huge	sample text
\Huge	sample text

LaTeX command	Equivalent switch	Output style	Remarks
\textnormal{...}	{\normalfont ...}	document font family	This is the default or normal font.
\emph{...}	{\em ...}	emphasis	Typically italics. Using emph{} inside of italic text removes the italics on the emphasized text.
\textrm{...}	{\rmfamily ...}	roman font family	
\textsf{...}	{\sffamily ...}	sans serif font family	
\texttt{...}	{\ttfamily ...}	teletypefont family	This is a fixed-width or monospace font.
\textup{...}	{\upshape ...}	upright shape	The same as the normal typeface.
\textit{...}	{\itshape ...}	italic shape	
\textsl{...}	{\slshape ...}	slanted shape	A skewed version of the normal typeface (similar to, but slightly different from, italics).
\textsc{...}	{\scshape ...}	Small Capitals	
\uppercase{...}		UPPERCASE (ALL CAPS)	Also \lowercase. There are some caveats, though; see here.
\textbf{...}	{\bfseries ...}	bold	
\textmd{...}	{\mdseries ...}	medium weight	The normal font weight.
\textlf{...}	{\lfseries ...}	light	A font weight lighter than normal. Not supported by all typefaces.
\textsubscript{} and \textsuperscript{}
\ldots



Command	Sample	Character
\%	{\displaystyle \%} \%	%
\$	{\displaystyle \$} \$	$
\{	{\displaystyle \{} \{	{
\_	{\displaystyle \_} \_	_
\P	{\displaystyle \P } \P 	¶
\ddag	n/a	‡
\textbar	n/a	|
\textgreater	{\displaystyle >} >	>
\textendash	n/a	–
\texttrademark	n/a	™
\textexclamdown	n/a	¡
\textsuperscript{a}	{\displaystyle \mathrm {X^{a}} } {\mathrm  {X^{{a}}}}	a
\pounds	n/a	£
\#	{\displaystyle \#} \#	#
\&	{\displaystyle \&} \&	&
\}	{\displaystyle \}} \}	}
\S	{\displaystyle \S } \S 	§
\dag	n/a	†
\textbackslash	n/a	\
\textless	{\displaystyle <} <	<
\textemdash	n/a	—
\textregistered	n/a	®
\textquestiondown	n/a	¿
\textcircled{a}	n/a	ⓐ
\copyright	n/a	©




LaTeX command	Sample	Description
\`{o}	ò	grave accent
\'{o}	ó	acute accent
\^{o}	ô	circumflex
\"{o}	ö	umlaut, trema or dieresis
\H{o}	ő	long Hungarian umlaut (double acute)
\~{o}	õ	tilde
\c{c}	ç	cedilla
\k{a}	ą	ogonek
\l{}	ł	barred l (l with stroke)
\={o}	ō	macron accent (a bar over the letter)
\b{o}	o	bar under the letter
\.{o}	ȯ	dot over the letter
\d{u}	ụ	dot under the letter
\r{a}	å	ring over the letter (for å there is also the special command \aa)
\u{o}	ŏ	breve over the letter
\v{s}	š	caron/háček ("v") over the letter
\t{oo}	o͡o	"tie" (inverted u) over the two letters
\o	ø	slashed o (o with stroke)

\usepackage[gen]{eurosym}


Input	Output	Purpose
-	-	inter-word
--	–	page range, 1–10
---	—	punctuation dash—like this
$-$	−	minus sign
