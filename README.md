A Typst document template styled after [*Arknights: Endfield*](https://endfield.gryphline.com/en-us#operator) by Hypergryph. Mainly designed for A4 document.

## Preview

![Cover page](img/cover.png)
![Sample content page](img/Page_3.png)

## Usage

Initialize a new project from the template:

```
typst init @preview/endfield-doc:0.1.2
```

Or import the template directly in an existing file:

```typst
#import "@preview/endfield-doc:0.1.2": endfield-doc

#show: endfield-doc.with(
  title:       [Document Title],
  subtitle:    [Subtitle],
  author:      [Author Name],
  date:        datetime.today().display("[year]-[month]-[day]"),
  institution: [Institution],
  doc-footer:  [Your Organization],
  lang:        "zh",
  region:      "cn",
)

= Introduction

Your document begins here. Text flows automatically across pages.

== A subsection

Level-2 and level-3 headings are also supported.

=== A third-level heading

Inline `code` and block code are styled automatically.

Math equations work out of the box:

$ E = m c^2 $
```

## Parameters

All parameters of `endfield-doc` are optional and have sensible defaults.

| Parameter | Type | Default | Description |
|---|---|---|---|
| `title` | content | `[Document Title]` | Document title — shown on the cover page and in every page header. |
| `subtitle` | content / `none` | `none` | Subtitle shown below the title on the cover page. |
| `author` | content / `none` | `none` | Author(s) shown on the cover page. Footnotes are supported. |
| `date` | content / `none` | `none` | Date shown on the cover page. |
| `institution` | content / `none` | `none` | Institution shown on the cover page. |
| `paper` | string | `"a4"` | Paper size passed to Typst's `page()`. Any Typst-supported value is accepted (e.g. `"a5"`, `"b5"`, `"us-letter"`). See [Known Limitations](#known-limitations). |
| `doc-footer` | content | `[ENDFIELD INDUSTRIES]` | Text shown on the left side of the footer bar. |
| `lang` | string | `"zh"` | Document language (passed to `set text`). |
| `region` | string | `"cn"` | Document region (passed to `set text`). |
| `font-cjk` | array | `("HarmonyOS Sans SC", "HarmonyOS Sans Italic")` | CJK font fallback list. |
| `font-latin` | array | `("HarmonyOS Sans", "HarmonyOS Sans Italic")` | Latin font fallback list. |
| `font-code` | array | `("JetBrains Mono", "Consolas")` | Monospace font fallback list for code blocks. |
| `font-emoji` | array | `("Segoe UI Emoji", "Noto Emoji")` | Emoji font fallback list. |

## Known Limitations

- **Page size**: the template is designed and visually tuned for A4. Passing a different `paper` value (e.g. `"a5"`) is supported but margins, font sizes, and spacing are not automatically rescaled. Manual adjustments are recommended for non-A4 sizes.
- **CJK Italic fonts**: Italic fonts for CJK characters are not handled properly, latin italic fonts are supported.

## License

MIT License. See [LICENSE](LICENSE) for details.

## Acknowledgements

- *Arknights: Endfield* by Hypergryph
- *typst-touying-theme-endfield* by [@leostudiooo](https://github.com/leostudiooo/typst-touying-theme-endfield)