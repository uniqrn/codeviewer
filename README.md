# codeviewer

[Hugo](https://gohugo.io/) theme for source code viewer, using [highlight.js](https://highlightjs.org/) and [highlightjs-line-numbers](https://github.com/wcoder/highlightjs-line-numbers.js/) for syntax highlighting.

## Settings

Hugo has its own [Highlight](https://gohugo.io/getting-started/configuration-markup#highlight) feature enabled by default.
It conflicts with highlight.js. You can disable hugo's highlight with `config.toml` site settings.

You can also customize highlight.js look and feel in `Params` section.

```toml
[markup.highlight]
codeFences = false                 # disable Hugo highlighting with Chroma

[Params]
color_scheme = "light"             # dark(default) | light
highlight_theme = "atom-one-dark"  # highlightjs theme name
```

Available `highlight_theme` is listed on highlight.js site.

* [Theme list](https://github.com/highlightjs/highlight.js/tree/main/src/styles)
* [Demo](https://highlightjs.org/static/demo/)

## Markdown Converter

This theme includes [code2md](./bin/code2md) script written in bash.

```bash
# Example Command
$ ./bin/code2md some_project/src/ hugo_site/content/
```

`code2md` reads source codes under specified directory, and simply puts markdown with code fences.  
With generated markdown, you can run `hugo` as usual.
