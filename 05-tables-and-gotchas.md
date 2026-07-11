# Tables and gotchas

Tables use pipes to separate columns and a divider row of dashes under the header, and this is where most people hit the syntax they can never remember. Tables are a GitHub Flavored Markdown extension, so plain CommonMark renderers may show them as raw pipes.

## Tables

The header row, a divider row, then data rows:

```
| Name  | Role     |
| ----- | -------- |
| Ada   | engineer |
| Grace | admiral  |
```

Colons in the divider row set alignment: `:---` left, `:--:` center, `---:` right.

```
| left | center | right |
| :--- | :----: | ----: |
| a    | b      | c     |
```

The outer pipes and perfect spacing are optional; renderers only need the pipes between cells and the dashed divider row. To put a literal pipe inside a cell, escape it as `\|`.

## Escaping

Backslash before a Markdown character makes it literal instead of active:

```
\*not italic\*
\# not a heading
1\. not a list item
```

This is how you show the syntax itself, or stop a leading number and period from starting a list.

## Hard line breaks

A single newline in the source usually does not create a line break in the output; the two lines get joined into one paragraph. To force a break, end the line with two trailing spaces, or use a backslash:

```
line one  
line two
```

The two-space method is invisible and easy to strip by accident, so many people prefer the trailing backslash or just a blank line to start a new paragraph.

## Blank lines matter

Blank lines separate blocks. A list, a code fence, or a heading placed directly against a paragraph with no blank line above it can fail to render or absorb the neighboring text. When something renders wrong, checking for a missing blank line fixes it more often than any other single thing.
