# latex-environments

## Overview

This is Quarto extension that enables `divs` to be output as a custom environment in LaTeX. This is useful when you'd like to share content between LaTeX and other formats, but need the content to be placed in an environment when emitting LaTeX.

## Installation

To install this extension in your current directory (or into the Quarto project that you're currently working in),  use the following command:

```
quarto install extension dragonstyle/latex-environments
```

## Usage

Divs with a class name listed in the in the `environments` key will be emitted in LaTeX as an environment with the provided name (or the class name itself if no name is provided). All of the following are valid:

```yaml
environments: program

environments:
  - program

environments: [program]

environments:
  program: program-env
```

## Example

```markdown
---
title: Test document
environments: [program]
----

:::{.program}
The contents of this div will be output in a `program`
latex environment, but will appear in HTML (and any other output 
format as a simple div with the class `program`)
:::
```
