# Notes-block Extension For Quarto

This extension makes it easy to add table and figure notes to Quarto output. At the moment this works only for PDF outputs from LaTeX.

## Installing

```bash
quarto add https://github.com/simonreif/notes-block
```

This will install the extension under the `_extensions` subdirectory.
If you're using version control, you will want to check in this directory.

## Using

You open a notes block below your figure or table using

```
::: {.notes-block}
**Notes:** These are the notes.
:::
```

You can specify the width as well as the distance reduced above and below the notes. Usually LaTeX puts quite some whitespace below figures and often not very much below the nots. These inputs can be used to make the output look more conscise.

The default for these settings is

```
::: {.notes-block width = "1" above = "-5" below = "15"}
**Notes:** These are the notes.
:::
```

where

- `width` is multuplied with `\textwidth`, so 0.5 is half the textwidth
- `above` uses `\vspace` with `pt` as the unit
- `below` uses `\vspace` with `pt` as the unit

## Example

Here is the source code for a minimal example: [example.qmd](example.qmd).
