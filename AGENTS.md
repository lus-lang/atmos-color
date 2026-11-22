# AGENTS.md

`lus-lang/atmos-color` is the repository of the `color` package of the atmosphere registry. Programs load the package with `require("https://atmosp.here/2.0/color.lus")`.

## Scope

`color` styles terminal text with ANSI escape sequences and writes plain text when the environment turns colors off. The public API is every function that `color.lus` returns in its module table. A change to that API needs a new entry in `CHANGELOG.md` and a version change in the header.

## Layout

- `color.lus` is the whole package. Its header doc comment contains the package metadata and the declared permissions.
- `tests/*_test.lus` are the tests. They load `color.lus` from the parent of `TEST_DIR`, the directory that holds the test file.

## Dependencies

None.

## Commands

Run these commands from the root of the repository.

```sh
lus test tests          # run the tests
lus check color.lus     # lint
lus doc color.lus       # print the reference
```

## Rules

- Every public function has a doc comment that states each result and each error, following `spec/design/style.md` of the Lus repository.
- The package never calls `pledge`. A new permission is declared in the header and in the README.
- Prose follows the `lus-writing` skill, which `lus agents init` installs and https://lus.dev/agents/skills/lus-writing/SKILL.md serves. In particular, prose has no dashes or semicolons and never names the Roblox Lua dialect.
- Every bug fix comes with a test that fails without it.
