# My Visual Studio Code (VSCode) workflow/setup

<!-- TOC -->

- [My Visual Studio Code (VSCode) workflow/setup](#my-visual-studio-code-vscode-workflowsetup)
  - [Extensions](#extensions)
    - [General](#general)
    - [Git-GitHub](#git-github)
    - [Markdown](#markdown)
    - [reStructuredText](#restructuredtext)
    - [LaTeX](#latex)
    - [Jupyter notebooks](#jupyter-notebooks)
    - [Python](#python)
    - [Julia](#julia)
  - [Snippets](#snippets)

<!-- /TOC -->

[Visual Studio Code (VSCode)](https://code.visualstudio.com/) is free, open-source, and there is a huge community developing extensions that will ease your writing and coding experience, and thus improve your productivity.

## Extensions

Below is a list of extensions that greatly simplifies my writing/coding workflow and improve my productivity.
All registered extensions are available on [VSCode's Marketplace](https://marketplace.visualstudio.com/vscode).
Extensions can also be installed locally from your VSCode window, see the [documentation](https://code.visualstudio.com/docs/editor/extension-marketplace).

### General

- https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode
- https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer-2
- https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments
- https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker
- https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker-french

### Git-GitHub

[git](https://git-scm.com/)
[GitHub](https://github.com/)

- https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory
- https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens
- https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github

### Markdown

[Markdown](https://en.wikipedia.org/wiki/Markdown) is a simple and lightweight markup language (`.md` files) that you may use to

- take notes
- write documentation
  - `README.md` files
  - [Python documentation with sphinx](https://www.sphinx-doc.org/en/master/usage/markdown.html)
  - [MkDocs](https://www.mkdocs.org/)
  - [Julia documentation](https://docs.julialang.org/en/v1/stdlib/Markdown/)
- update your webpage, see, e.g., https://cristal-sigma.github.io/
- ...

Suggested VSCode extensions:

- https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one
- https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint
- https://marketplace.visualstudio.com/items?itemName=huntertran.auto-markdown-toc

### reStructuredText

[reStructuredText](https://en.wikipedia.org/wiki/ReStructuredText) is a markup language (`.rst` files) that you may use to

- take notes
- write documentation
  - `README.rst` files
  - [Python documentation with sphinx](https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html)
- ...

Suggested VSCode extensions:

- https://marketplace.visualstudio.com/items?itemName=lextudio.restructuredtext

### LaTeX

[LaTeX](https://en.wikipedia.org/wiki/LaTeX) is primarily used in academia to

- take notes
- make Beamer presentations
- make posters
- write scientific papers
- write your CV
- ...

Suggested VSCode extensions:

- https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop

### Jupyter notebooks

[Jupyter](https://jupyter.org/) notebook can be used to

- prototype some code
- illustrate some code
- create course material
- ...

Suggested VSCode extensions:

- https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter

### Python

A good [Python](https://www.python.org/) code setup ease your coding experience and brings clarity in collaborative projects

[VSCode Python Tutorial](https://code.visualstudio.com/docs/python/python-tutorial)

- https://marketplace.visualstudio.com/items?itemName=ms-python.python
- https://marketplace.visualstudio.com/items?itemName=KevinRose.vsc-python-indent
- https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring
- https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance
- https://marketplace.visualstudio.com/items?itemName=tamasfe.even-better-toml

### Julia

A good [Julia](https://julialang.org/) code setup ease your coding experience and brings clarity in collaborative projects

- https://marketplace.visualstudio.com/items?itemName=julialang.language-julia
- https://marketplace.visualstudio.com/items?itemName=cameronbieganek.julia-color-themes
- https://marketplace.visualstudio.com/items?itemName=colinfang.markdown-julia
- https://marketplace.visualstudio.com/items?itemName=tamasfe.even-better-toml

## Snippets

> [Code snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets) are templates that make it easier to enter repeating code patterns, such as loops or conditional-statements.

Many language-specific [extensions](#extensions) already provide some useful snippets.
While some of them exactly match your needs, some others might be missing or you may not remember how to trigger them.

For these reasons you may create your own snippets to increase your productivity.
Open the Command Palette (`CMD + Maj + P`) and type `Configure User Snippets`, you can then choose to create language-specific snippets or create generic snippets that can be triggered in different scopes.

The file [`guilgautier.code-snippets`](#guilgautier.code-snippets) contains some snippets I frequently use and find very convenient.
