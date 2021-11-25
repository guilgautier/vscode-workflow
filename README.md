# My Visual Studio Code (VSCode) workflow/setup

- [My Visual Studio Code (VSCode) workflow/setup](#my-visual-studio-code-vscode-workflowsetup)
  - [Install the `code` shell command](#install-the-code-shell-command)
  - [Two levels of configuration](#two-levels-of-configuration)
    - [Settings synchronization](#settings-synchronization)
  - [Settings](#settings)
  - [Snippets](#snippets)
  - [Test and debug code within VSCode](#test-and-debug-code-within-vscode)
    - [Debug Python](#debug-python)
  - [Tasks](#tasks)
  - [Extensions](#extensions)
    - [General](#general)
    - [Git-GitHub](#git-github)
    - [Markdown](#markdown)
    - [reStructuredText](#restructuredtext)
    - [LaTeX](#latex)
    - [Jupyter notebooks](#jupyter-notebooks)
    - [Python](#python)
    - [Julia](#julia)

[Visual Studio Code (VSCode)](https://code.visualstudio.com/) is free, open-source, and there is a huge community developing extensions that will ease your writing and coding experience, and thus improve your productivity.

## Install the `code` shell command

The `code` shell command allows you to open a file with VSCode, install an extension, etc. from the command line.

To make the `code` command available in your shell, open the Command Palette (`CMD + Shift + P`) and type `shell command`, see also [Launching from the command line](https://code.visualstudio.com/docs/setup/mac#_launching-from-the-command-line).

## Two levels of configuration

1. On a per project basis, at the root of your project/workspace, the `.vscode` folder contains some local VSCode configuration files like

   - [extensions.json](./extensions.json),
   - [launch.json](./launch.json),
   - [settings.json](./settings.json),
   - [tasks.json](./tasks.json),
   - [guilgautier.code-snippets](./guilgautier.code-snippets).

2. VSCode can be configured globally at the user level as described in the following sections.

### Settings synchronization

You may also consider [synchronizing your settings](https://code.visualstudio.com/docs/editor/settings-sync), in order to keep the same setup each time you log in VS Code (from a different machine for example).

## Settings

> [VSCode settings](https://code.visualstudio.com/docs/getstarted/settings) You can configure Visual Studio Code to your liking through its various settings. Nearly every part of VS Code's editor, user interface, and functional behavior has options you can modify.

To edit your personal settings, open the Command Palette (`CMD + Shift + P`) and type `Open Settings (JSON)`.

The file [settings.json](./settings.json) contains my favorite settings.
**Note:** Some settings only apply to some [extensions](#extensions) suggested below.

## Snippets

> [Code snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets) are templates that make it easier to enter repeating code patterns, such as loops or conditional-statements.

Many language-specific [extensions](#extensions) already provide some useful snippets.
While some of them exactly match your needs, some others might be missing or you may not remember how to trigger them.
For these reasons you may create your own snippets to increase your productivity.

To create your personal snippets, open the Command Palette (`CMD + Shift + P`) and type `Configure User Snippets`.
You can then choose to create:

- language-specific snippets, or
- generic snippets,

that can be triggered within different scopes (python, julia, markdown, ect.).

The file [guilgautier.code-snippets](./guilgautier.code-snippets) contains some snippets I frequently use and find super convenient.

## Test and debug code within VSCode

[General debugging](https://code.visualstudio.com/docs/editor/debugging)

### Debug Python

The [.vscode/launch.json](launch.json) file contains two configurations for debugging

1. Python generic `.py` files,
2. Python test files `tests/test_XXX.py`.

For more details, check out the documentation:

- [Testing](https://code.visualstudio.com/docs/python/testing),
- [Debugging](https://code.visualstudio.com/docs/python/debugging),
- [Debug Tests](https://code.visualstudio.com/docs/python/testing#_debug-tests).

## Tasks

> Lots of tools exist to automate [tasks](https://code.visualstudio.com/docs/editor/tasks) like linting, building, packaging, testing, or deploying software systems.

To create your personal tasks, open the Command Palette (`CMD + Shift + P`) and type `Tasks: Open User Tasks`,

The [`tasks.json`](./tasks.json) file contains some tasks I frequently use and find super convenient, like building the documentation of my Python/Julia project, running tests, etc.
This file can be thought of as the VSCode counter part of a Makefile.

To run your favorite task open the Command Palette (`CMD + Shift + P`) and type `Tasks: Run Task`.
Tasks defined as `"kind": "build"`, can be run simply using `CMD + Shift + B`.

## Extensions

The file [extensions.json](./extensions.json) contains a suggestive list of VSCode extensions that greatly simplify my writing/coding workflow and improve my productivity.

All registered extensions are available on [VSCode's Marketplace](https://marketplace.visualstudio.com/vscode).
Extensions can also be installed locally from your VSCode window, see the [documentation](https://code.visualstudio.com/docs/editor/extension-marketplace).

To install the the extensions listed and detailed in the next sections you can execute the following code block in your Terminal.

Make sure you have [installed the `code` shell command](#install-the-code-shell-command).

```bash
  code --install-extension <extension-name>
```

### General

- <https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode>
- <https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense>
- <https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer-2>
- <https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments>
- <https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker>
- <https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker-french>
- <https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare>

```bash
code --install-extension VisualStudioExptTeam.vscodeintellicode
code --install-extension christian-kohler.path-intellisense
code --install-extension CoenraadS.bracket-pair-colorizer-2
code --install-extension aaron-bond.better-comments
code --install-extension streetsidesoftware.code-spell-checker
code --install-extension streetsidesoftware.code-spell-checker-french
code --install-extension MS-vsliveshare.vsliveshare
```

### Git-GitHub

[git](https://git-scm.com/)
[GitHub](https://github.com/)

- <https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory>
- <https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens>
- <https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github>

```bash
code --install-extension donjayamanne.githistory
code --install-extension eamodio.gitlens
code --install-extension GitHub.vscode-pull-request-github

code --install-extension redhat.vscode-yaml
```

### Markdown

[Markdown](https://en.wikipedia.org/wiki/Markdown) is a simple and lightweight markup language (`.md` files) that you may use to

- take notes
- write documentation
  - `README.md` files
  - [Python documentation with sphinx](https://www.sphinx-doc.org/en/master/usage/markdown.html)
  - [MkDocs](https://www.mkdocs.org/)
  - [Julia documentation](https://docs.julialang.org/en/v1/stdlib/Markdown/)
- update your webpage, see, e.g., <https://cristal-sigma.github.io/>
- ...

Suggested VSCode extensions:

- <https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one>
- <https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint>
- <https://marketplace.visualstudio.com/items?itemName=shuworks.vscode-table-formatter>

```bash
code --install-extension yzhang.markdown-all-in-one
code --install-extension DavidAnson.vscode-markdownlint
code --install-extension shuworks.vscode-table-formatter
```

### reStructuredText

[reStructuredText](https://en.wikipedia.org/wiki/ReStructuredText) is a markup language (`.rst` files) that you may use to

- take notes
- write documentation
  - `README.rst` files
  - [Python documentation with sphinx](https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html)
- ...

Suggested VSCode extensions:

- <https://marketplace.visualstudio.com/items?itemName=lextudio.restructuredtext-pack>

```bash
code --install-extension llextudio.restructuredtext-pack
```

### LaTeX

[LaTeX](https://en.wikipedia.org/wiki/LaTeX) is primarily used in academia to

- take notes
- make Beamer presentations
- make posters
- write scientific papers
- write your CV
- ...

Suggested VSCode extensions:

- <https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop>

```bash
code --install-extension James-Yu.latex-workshop
```

### Jupyter notebooks

[Jupyter](https://jupyter.org/) notebook can be used to

- prototype some code
- illustrate some code
- create course material
- ...

Suggested VSCode extensions:

- <https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter>

```bash
code --install-extension ms-toolsai.jupyter
```

### Python

A good [Python](https://www.python.org/) code setup ease your coding experience and brings clarity in collaborative projects

[VSCode Python Tutorial](https://code.visualstudio.com/docs/python/python-tutorial)

- <https://marketplace.visualstudio.com/items?itemName=ms-python.python>
- <https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance>
- <https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring>
- <https://marketplace.visualstudio.com/items?itemName=KevinRose.vsc-python-indent>

- <https://marketplace.visualstudio.com/items?itemName=lextudio.restructuredtext-pack>
- <https://marketplace.visualstudio.com/items?itemName=shuworks.vscode-table-formatter>

- <https://marketplace.visualstudio.com/items?itemName=tamasfe.even-better-toml>

```bash
code --install-extension ms-python.python
code --install-extension ms-python.vscode-pylance
code --install-extension njpwerner.autodocstring
code --install-extension KevinRose.vsc-python-indent

code --install-extension lextudio.restructuredtext-pack
code --install-extension shuworks.vscode-table-formatter

code --install-extension tamasfe.even-better-toml
```

### Julia

A good [Julia](https://julialang.org/) code setup ease your coding experience and brings clarity in collaborative projects

- <https://marketplace.visualstudio.com/items?itemName=julialang.language-julia>
- <https://marketplace.visualstudio.com/items?itemName=cameronbieganek.julia-color-themes>
- <https://marketplace.visualstudio.com/items?itemName=singularitti.vscode-julia-formatter>

- <https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one>
- <https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint>
- <https://marketplace.visualstudio.com/items?itemName=shuworks.vscode-table-formatter>
- <https://marketplace.visualstudio.com/items?itemName=colinfang.markdown-julia>

- <https://marketplace.visualstudio.com/items?itemName=tamasfe.even-better-toml>

```bash
code --install-extension julialang.language-julia
code --install-extension cameronbieganek.julia-color-themes
code --install-extension singularitti.vscode-julia-formatter

code --install-extension yzhang.markdown-all-in-one
code --install-extension DavidAnson.vscode-markdownlint
code --install-extension shuworks.vscode-table-formatter
code --install-extension colinfang.markdown-julia

code --install-extension tamasfe.even-better-toml
```
