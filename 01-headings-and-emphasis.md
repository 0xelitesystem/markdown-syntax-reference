# Headings and emphasis

Headings use one to six `#` characters at the start of a line, and emphasis uses `*` or `_` around text. The count of hash marks sets the level: `#` is an H1, `##` is an H2, down to `######` for an H6. You need a space after the hash marks, and headings must sit on their own line.

## Headings

```
# H1 title
## H2 section
### H3 subsection
```

There is also an older underline style for the top two levels, where a line of `=` under text makes an H1 and a line of `-` makes an H2:

```
Title
=====

Section
-------
```

The hash style is more common because it works for all six levels and reads clearly.

## Bold and italic

Wrap text in one marker for italic and two for bold. Both `*` and `_` work:

```
*italic* or _italic_
**bold** or __bold__
***bold italic***
```

Use the asterisk form when the emphasis is in the middle of a word, because underscores inside a word (like `snake_case`) are often not treated as emphasis, which is usually what you want.

## Strikethrough

GitHub Flavored Markdown adds strikethrough with two tildes:

```
~~no longer true~~
```

This is not part of the original Markdown, so plain CommonMark renderers may show the tildes literally.

## Horizontal rule

Three or more `-`, `*`, or `_` on their own line draw a horizontal rule:

```
---
```

Leave a blank line before it. If the line above is text, a row of dashes is read as a heading underline instead of a rule, which is a frequent surprise.

## Combining emphasis

You can nest emphasis by mixing the markers, which is why the asterisk and underscore forms are both useful. Putting bold inside italic (or the reverse) works when the inner and outer markers differ, so the parser can tell them apart:

```
*italic with **bold** inside*
```

Keep emphasis on a single line. A `*` that opens on one line and never closes before the paragraph ends is left as a literal asterisk, another common cause of text that renders with stray symbols.
