# Quarto nf-core template

This repository contains a simple [Quarto](https://quarto.org/) template for use
in nf-core HTML reports and nf-core presentations. Quarto works with both Python and R
out of the box, as well as for both HTML/PDF reports and revealjs-based
presentations.

## Installation

If you've already installed Quarto you can install the template like so:

```bash
quarto use template fasterius/nf-core-quarto-template
```

This will install the template (_i.e._ create the `_extensions/` directory in
your current location) and create an example `.qmd` file that you can use as a
starting place for your report. You can also just install the template itself
without getting the `.qmd` file like so:

```bash
quarto add fasterius/nf-core-quarto-template
```

## Usage

After a successful installation you can use the template by specifying _e.g._
the HTML format in your YAML header, like so:

```yaml
...
format:
    nf-core-html: default
...
```

You can also use the included `reveal.js` format:

```yaml
...
format:
    nf-core-revealjs: default
...
```

The template uses the nf-core colours for _e.g._ table of contents, inline code and
syntax highlighting. You can check the default format specifications in the
`_extension.yml` file, which can be overridden by your own YAML header, like so:

```yaml
...
format:
    nf-core-html:
        embed-resources: false
        highlight-style: arrow
...
```

You can find a minimal example in the [template.qmd](template.qmd) file. While
the example is using R and the `knitr` engine you can easily use a Jupyter
kernel instead by specifying _e.g._ `jupyter: python3`.
