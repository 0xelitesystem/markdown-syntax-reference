# Lists and task lists

Unordered lists start each line with `-`, `*`, or `+`, and ordered lists start with a number followed by a period. You need a space after the marker. A blank line before the first item separates the list from the paragraph above it.

## Unordered and ordered

```
- first
- second
- third

1. first
2. second
3. third
```

For ordered lists the actual numbers do not have to be correct. Most renderers renumber automatically, so a list written `1.` `1.` `1.` still shows as 1, 2, 3. Writing every item as `1.` makes reordering painless.

## Nesting

Indent a child item under its parent. Two to four spaces work; the safest rule is to indent the child so it lines up past the parent marker:

```
- parent
  - child
    - grandchild
- next parent
```

Inconsistent indentation is the top cause of lists that render flat or break into separate lists. Pick two or four spaces and stay consistent.

## Multi-line items

To put a paragraph or code block inside a list item, indent the continued content to match the text of the item:

```
1. Step one.

   A second paragraph inside step one.

2. Step two.
```

## Task lists

GitHub Flavored Markdown adds checkboxes. Use a list item with `[ ]` for unchecked and `[x]` for checked, with a space inside the brackets:

```
- [ ] not done
- [x] done
```

These render as clickable checkboxes on GitHub and similar tools. On plain CommonMark renderers they show as literal brackets, since task lists are an extension rather than core syntax.
