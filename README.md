# MisTex
MisTex is a LaTeX renderer for mistune, allowing for the creation of
LaTeX documents from Markdown files.

This project also includes an 'escape' mistune plugin to aid in
including raw latex.

## Usage
~~~python
import mistune
from MisTex.Renderer import Renderer
# Always use this if you want raw latex beyond simple $ and $$
# anywhere in the input
from MisTex.Escape import escape

# Create parser
markdown = mistune.create_markdown(renderer=Renderer(), plugins=[escape])
# Parse
markdown("**Bold Text**")
~~~

## Some notes
Write CommonMark compatible Markdown and you'll generally have a good time.
If you want to include some raw LaTeX in your document, add the 'escape' plugin
and do the following.
~~~
^^^
Raw Latex Here...
^^^
~~~
This ensures that we don't accidentally treat the raw LaTeX as
Markdown.
