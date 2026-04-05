# Arknights: Endfield Typst Template for Documentation

This is a Typst document template inspired by the art style of [*Arknights: Endfield*](https://endfield.gryphline.com/en-us#operator), a video game by Hypergryph. The template directly references another Endfield-style Typst [Touying](https://github.com/touying-typ/touying) template by [@leostudiooo](https://github.com/leostudiooo/typst-touying-theme-endfield.git).

## Preview

![Cover](thumbnail.png)
![Sample Page](img/Page_3.png)

## Usage

The template has not been uploaded to the Typst package registry yet, so you can copy the `lib.typ` file into your project and import it as shown below. You can customize the fields in the `#show: endfield-doc.with(...)` block as needed.

```typst
#import "@preview/endfield-doc:0.1.0": endfield-doc

#show: endfield-doc.with(
  title:       [Document Title],
  subtitle:    [Subtitle],
  author:      [Author Name],
  date:        datetime.today().display("[year]-[month]-[day]"),
  institution: [Institution],
  doc-footer:  [Your Footer Text],
  lang:        "en",
  region:      "us",
  // font-cjk:   ("HarmonyOS Sans SC",),
  // font-latin: ("HarmonyOS Sans",),
  // font-code:  ("JetBrains Mono", "Consolas"),
  // font-emoji: ("Segoe UI Emoji", "Noto Emoji"),
)

= Introduction

Your document begins here. Text flows automatically across pages.

```

## Acknowledgements

- _Arknights: Endfield_
- _typst-touying-theme-endfield_ by [@leostudiooo](https://github.com/leostudiooo/typst-touying-theme-endfield)