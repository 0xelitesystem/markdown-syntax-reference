# Links and images

An inline link is `[visible text](url)`, and an image is the same with a leading `!`. The text in brackets is what the reader sees, and the URL in parentheses is where it points. An optional title in quotes after the URL becomes hover text.

## Inline links

```
[GitHub](https://github.com)
[with a title](https://github.com "hover text")
```

The URL can be absolute (`https://...`) or relative to the current file (`./docs/setup.md`). Relative links are how you connect files inside a repo.

## Reference links

When the same URL is used many times, or you want to keep prose clean, define the link once and refer to it by label:

```
See the [docs][d] and the [guide][d].

[d]: https://example.com/docs
```

The label is case-insensitive and the definition can sit anywhere in the document, usually at the bottom. If the label matches the visible text you can shorten it to `[docs][]` or just `[docs]` with a matching `[docs]: url` definition.

## Images

An image is a link with a `!` in front. The bracket text is the alt text, which shows if the image fails to load and is read by screen readers:

```
![alt text describing the image](path/to/image.png)
![logo](./assets/logo.svg "optional title")
```

Always write meaningful alt text. Empty alt (`![]`) is only correct for purely decorative images.

## Autolinks

A bare URL in angle brackets becomes a clickable link:

```
<https://example.com>
<name@example.com>
```

GitHub Flavored Markdown also linkifies bare URLs without the brackets, but plain CommonMark does not, so the angle brackets are the portable form.
