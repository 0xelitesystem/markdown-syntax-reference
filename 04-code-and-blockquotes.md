# Code and blockquotes

Inline code uses single backticks around text, and a code block uses three backticks on their own lines above and below. Code spans and blocks turn off Markdown formatting inside them, so characters like `*` and `_` appear literally instead of becoming emphasis.

## Inline code

Wrap a snippet in backticks to render it in a monospace span:

```
Run `npm install` first.
```

If the code itself contains a backtick, wrap it in a longer run of backticks so the fence is unambiguous:

``` 
Use `` `code` `` to show a backtick.
```

The rule is that the opening and closing runs must have the same number of backticks, and that number must be longer than any run inside.

## Fenced code blocks

Three or more backticks open and close a block. Put a language name right after the opening fence to get syntax highlighting:

```
```js
function add(a, b) {
  return a + b;
}
```
```

The language hint (`js`, `python`, `bash`, `json`, and so on) is optional but recommended. You can also fence with tildes (`~~~`), which is handy when the block itself contains triple backticks.

## Indented code blocks

Indenting a line by four spaces also makes a code block, a holdover from original Markdown:

```
    this is code
```

Fenced blocks are preferred because they support a language hint and do not fight with list indentation.

## Blockquotes

Prefix a line with `>` to quote it. Quotes can span multiple lines and can nest:

```
> A quoted line.
> Still the same quote.
>
> > A nested quote.
```

You can put other Markdown inside a quote, including lists and code blocks, by keeping the `>` prefix on each line.
