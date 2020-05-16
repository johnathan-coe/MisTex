# MisTex
MisTex is a LaTeX renderer for mistune, allowing for the creation of
LaTeX documents from Markdown files.

## Usage
~~~python
import mistune
from MisTex.Renderer import Renderer

markdown = mistune.create_markdown(renderer=Renderer())
markdown("**Bold Text**")
~~~

## Some notes
If you throw CommonMark compatible markdown into this, you will
generally have a good time. If you however, try to throw raw
LaTeX into the document, you may have an issue.

Throwing in equations with $x$ or $$x$$ generally won't hurt
if you don't use any "Markdown reserved" characters.

I'm in the process of making a plugin that will
"escape" Markdown and allow raw LaTeX in the input
document.
