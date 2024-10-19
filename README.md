# KAMK Typst Templates

Typst templates trying to copy the appearance of KAMK's official Word templates.

## Fonts

If you are **not** running Windows, you will have to install [Calibri](https://wiki.debian.org/ppviewerFonts) font, or alternatively [Carlito](https://fonts.google.com/specimen/Carlito) font.

Carlito is possibly already [packaged](https://pkgs.org/search/?q=carlito) for your system.

If you have correctly installed one of fonts, you can ignore Typst warning about missing the other.

## Project Plan

### Usage

Copy `comments.tmTheme`, `kamk-logo.png` and `project-plan.typ` to the directory of your Typst document,\
and then add something like the following piece of code at the start of it:

```typst
#import "project-plan.typ": project-plan

#show: doc => project-plan(
  date: auto,
  title: "Foobar",
  doc
)
```

### Parameters

| Parameter   | Type                 | Default         | Description             |
| ----------- | -------------------- | ----------------| ----------------------- |
| `author`    | Array, String        | `()`            |                         |
| `course`    | String               | `"Opintojakso"` |                         |
| `cover`     | String               | `""`            | Path to cover image.    |
| `date`      | Auto, Datetime, None | `none`          |                         |
| `degree`    | String               | `"Tutkinto"`    |                         |
| `keywords`  | Array, String        | `()`            |                         |
| `monospace` | String               | `"Monospace"`   | Font used for raw text. |
| `title`     | None, String         | `none`          |                         |

## License

MIT
