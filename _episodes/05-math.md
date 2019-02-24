---
title: LaTeX Math
teaching: 00
exercises: 00

questions:
- "How do I use equations in LaTeX?"

objectives:
- "Explain the way to activate math mode in-line and as an environment"
- "Render sample math text in LaTeX"
- "Learn how to represent some common symbols with math"
- "Apply superscripts, subscripts, and similar symbolic nomenclature"
- "Learn how to to properly employ braces"
- "Create fractions properly"
- "Align equations over multiple lines"
- "Break a long equation across multiple lines"

keypoints:
- "Activate the math environment with `equation`"
- "Activate the in-line math mode with `$`"
- "Use the math environment without creating a numbered equation using `equation*` and `[]`"
- "Enter Greek symbols such as `phi` with escape sequencies in math mode"
- "Distinguish super- and sub- levels of script with `^` and `_`"
- "Create an integral with `int` which is bound by text using `^` and `_`"
- "Recognize that mathematical symbols such as `cos` and `sin` must be escaped sequences"
- "Use `left(`, `right(`, and similar brace sequences to dynamically bound math"
- "Create fractions with the `frac` command instead of `/`"
- "Align a multistep sequence using the `align` and `split` environments using `&` helpers"
- "Include plaintext portions of aligned math using the `array` environment with `&{}` helpers"
- "Break a long equation up with `multline`"

---

#### Equalities

| Symbol |           Script         | Symbol |           Script         |
|:------:|:-------------------------|:------:|:-------------------------|
|   \=   | =                        |   ≠    | \neq                     |
|   ≐    | \doteq                   |   ≡    | \\equiv                  |
|   ≈    | \approx                  |   ≅    | \cong                    |
|   ≃    | \simeq                   |   ∼    | sim                      |



#### Inequalities

| Symbol |           Script         | Symbol |           Script         |
|:------:|:-------------------------|:------:|:-------------------------|
|   <    | <                        |   \>    | >                       |
|   ≤    | \leq                     |   ≥    | \geq                     |
|   ≪    | \ll                      |   ≫    | \gg                     |


#### Sets

| Symbol |           Script         | Symbol |           Script         |
|:------:|:-------------------------|:------:|:-------------------------|
|   ∈    | \in                      |   ∋    | \ni                      |
|   ∉    | \notin                   |   ¬    | \neg                     |
|   ∩    | \cap                     |   ∪    | \cup                     |
|   ⊓    | \sqcap                   |   ⊔    | \sqcup                   |
|   ∧    | \wedge \land             |   ∨    | \vee \lor                |
|   ∃    | \exists                  |   ∄    | \nexists                 |
|   ≀    | \wr                      |   ⊎    | \uplus                   |
|   ·    | \cdot                    |   ⋄    | \diamond                 |
|   △    | \bigtriangleup           |   ▽    | \bigtriangledown         |
|   ⊲    | \triangleleft            |   ⊳    | \triangleright           |
|       | \bigcirc                 |   •    | \bullet                  |
|   ∀    | \forall                  |

#### Set Equalities/Inequalities

| Symbol |           Script         | Symbol |           Script         |
|:------:|:-------------------------|:------:|:-------------------------|
|   ⊂    | \subset                  |   ⊃    | \supset                  |
|   ⊆    | \subseteq                |   ⊇    | \supseteq                |
|   ⊈    | \nsubseteq               |   ⊉    | \nsupseteq               |
|   ⊏    | \sqsubset                |   ⊐    | \sqsupset                |
|   ⊑    | \sqsubseteq              |   ⊒    | \sqsupseteq              |
|   ≼    | \preceq                  |   ≽    | \succeq                  |
|   ≺    | \prec                    |   ≻    | \succ                    |
|   ∝    | \propto                  |   ⊨    | \models                  |
|   ⊢    | \vdash                   |   ⊣    | \dashv                   |

#### Set Logic

| Symbol |           Script         | Symbol |           Script         |
|:------:|:-------------------------|:------:|:-------------------------|
|   →    | \rightarrow \to          |   ←    | \leftarrow \gets         |
|   ⇒    | \Rightarrow  \implies    |   ⇐    | \LeftRightarrow          |
|   ↔    | \leftrightarrow          |   ⇔    | \iff                     |
|   ⊤    | \top                     |   ⊥    | \bot                     |
|   ∅    | \emptyset                |   ⌀    | \varnothing              |
|   ↦    | \mapsto                  |        |                          |


#### Geometric Relationships

| Symbol |           Script         | Symbol |           Script         |
|:------:|:-------------------------|:------:|:-------------------------|
|   ∥    | \parallel                |   ∦    | \nparallel               |
|   ≍    | \asymp                   |   ⋈    | \bowtie                  |
|   ⏝    | \smile                   |   ⏜    | \frown                   |
|   ∡    | \sphericalangle          |   ∠    | \measuredangle           |
|   ⊥    | \perp                    |

#### Binary Operators

| Symbol |           Script         | Symbol |           Script         |
|:------:|:-------------------------|:------:|:-------------------------|
|   ±    | \pm                      |   ∓    | \mp                      |
|   ×    | \times                   |   ÷    | \div                     |
|   ∗    | \ast                     |   ⋆    | \star                    |
|   †    | \dagger                  |   ‡    | \ddagger                 |

| Symbol |           Script         | Symbol |           Script         |
|:------:|:-------------------------|:------:|:-------------------------|
|   ⊕    | \oplus                   |   ⊙    | \odot                    |
|   ⊖    | \ominus                  |   ∘    | \circ                    |
|   ⊗    | \otimes                  |   ∖    | \setminus                |
|   ⊘    | \oslash                  |       | \amalg                   |




#### Delimiters

| Symbol |           Script         | Symbol |           Script         |
|:------:|:-------------------------|:------:|:-------------------------|
|   ∣    | \mid                     |   ∣    | \mid                     |
|   ‖    | \|                       |   ‖    | \|                       |
|   {    | \{ \left{                |   }    | \} \right}               |
|   (    | \left(                   |   )    | \right)                  |
|   [    | \left[                   |   ]    | \right]                  |
|   ↑    | \uparrow                 |   ↓    | \downarrow               |
|   ⇑    | \Uparrow                 |   ⇓    | \Downarrow               |
|   ⟨    | \langle                  |   ⟩    | \rangle                  |
|   /    | /                        |   \    | \backslash               |
|   ⌈    | \lceil                   |   ⌉    | \rceil                   |
|   ⌊    | \lfloor                  |   ⌋    | \rfloor                  |


#### Greek Characters

|  Symbol  |              Script            |  Symbol  |             Script             |
|:--------:|:-------------------------------|:--------:|:-------------------------------|
|   𝛢 𝛼    | \Alpha \alpha                  |   𝛮 𝜈    | \Nu \nu                        |
|   𝛣 𝛽    | \Beta \beta                    |   𝛯 𝜉    | \Xi \xi                        |
|   𝛤 𝛾    | \Gamma \gamma                  |   𝛰 𝜊    | \Omicron \omicron              |
|   𝛥 𝛿    | \Delta \delta                  |   𝛱 𝜋 𝜛  | \Pi \pi \varpi                |
|   𝛦 𝜀 ϵ  | \Epsilon \epsilon \varepsilon  |   𝛲 𝜌 𝜚  | \Rho \rho \varrho              |
|   𝛧 𝜁    | \Zeta \zeta                    |   𝛴 𝜎    | \Sigma \sigma \varsigma        |
|   𝛨 𝜂    | \Eta \eta                      |   𝛵 𝜏    | \Tau \tau                      |
|   𝛩 𝜃 𝜗  | \Theta \theta \vartheta        |   𝛶 𝜐    | \Upsilon \upsilon              |
|   𝛪 𝜄     | \Iota \iota                    |   𝛷 𝜑 𝜙  | \Phi \phi \varphi              |
|   𝛫 𝜅 𝜘  | \Kappa \kappa \varkappa        |   𝛸 𝜒    | \Chi \chi                      |
|   𝛬 𝜆    | \Lambda \lambda                |   𝛹 𝜓    | \Psi \psi                      |
|   𝛭 𝜇    | \Mu \mu                        |   𝛺 𝜔    | \Omega \omega                  |



#### n-ArrayOperators, Functions, Integrals, and Other Characters

| Symbol |           Script         | Symbol |           Script         |
|:------:|:-------------------------|:------:|:-------------------------|
|   ∂    | \partial                 |   ∑    | \sum                     |
|   ð    | \eth                     |   ∏    | \prod                    |
|   ℏ    | \hbar                    |   ∐    | \coprod                  |
|       | \imath                    |   ⨁    | \bigoplus                |
|       | \jmath                    |   ⨂    | \bigotimes               |
|   ℓ    | \ell                      |   ⨀    | \bigodot                 |
|   ℜ    | \Re                      |   ⋃    | \bigcup                  |
|   ℑ    | \Im                      |   ⋂    | \bigcap                  |
|   ℘    | \wp                      |   ⨄    | \biguplus                |
|   ∇    | \nabla                   |   ⨆    | \bigsqcup                |
|   ☐    | \Box                     |   ⋁    | \bigvee                  |
|   ∞    | \infty                   |   ⋀    | \bigwedge                |
|   ∫    | \int                     |   ℵ    | \aleph                  |
|   ∮    | \oint                   |   ℶ    | \beth                    |
|   ∬    | \iint                    |   ℷ    | \gimel                   |
|   ∭    | \iiint                   |   ⨌    | \iiiint                 |
|   ∫⋯∫    | \idotsint              |





#### Trigonometric Functions (author's note, no Unicode equivalents)

| Symbol |   Script   | Symbol |   Script   | Symbol |   Script   | Symbol |   Script   |
|:------:|:-----------|:------:|:-----------|:------:|:-----------|:------:|:-----------|
|   sin  | \sin       |  sin⁻¹ | \arcsin    |  sinh  | \sinh      |   sec  | \sec       |
|   cos  | \cos       |  cos⁻¹ | \arccos    |  cosh  | \cosh      |   csc  | \csc       |
|   tan  | \tan       |  tan⁻¹ | \arctan    |  tanh  | \tanh      |
|   cot  | \cot       |  cot⁻¹ | \arccot    |  coth  | \coth      |




















