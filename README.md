# color

`color` styles terminal text with ANSI escape sequences and writes plain text when the environment turns colors off.

The following example prints an error label in bold red and a warning label in orange.

```lus nocheck
local color = require("https://atmosp.here/2.0/color.lus")

print(color.bold.red("error:") .. " file not found")
print(color.hex("#ff8800")("warning:") .. " disk almost full")
```

The package requires Lus 2.0 and declares the permission `env:read`, which it uses to read `NO_COLOR`, `FORCE_COLOR`, and `TERM`. It never calls `pledge`, so the program that loads it keeps control of its permissions.

The reference is in the doc comments of `color.lus`, which `lus doc color.lus` prints.
