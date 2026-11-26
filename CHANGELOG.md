# Changelog

## 1.0.0

**Release date:** TBD

Version 1.0.0 is the first release of `color`.

- Added the `color` package.
  - `color.red`, `color.bold`, and the other named styles: Wrap text in the escape codes of a style. Styles chain, as in `color.bold.red`.
  - `color.ansi256`, `color.rgb`, and `color.hex`: Return a style for a color of the 256-color palette or a 24-bit color.
  - `color.bg_ansi256`, `color.bg_rgb`, and `color.bg_hex`: Return the matching background styles.
  - `color.enable` and `color.enabled`: Turn escape codes on or off and report whether they are on.
  - `color.strip` and `color.width`: Remove escape sequences from text and count its characters without them.
