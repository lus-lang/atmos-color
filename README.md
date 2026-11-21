# color

Styles terminal text with ANSI escape sequences.

```lus nocheck
local color = require("https://atmosp.here/2.0/color.lus")

print(color.bold.red("error:") .. " file not found")
print(color.hex("#ff8800")("orange"))
```

The package requires Lus 2.0. It declares the permission env:read in its header. It calls no `pledge` of its own, so the program that loads it keeps control of its permissions.

The reference is in the doc comments of `color.lus`. Run `lus doc color.lus` to print it.
