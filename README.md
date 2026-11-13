# Destiny tools

Tools used to build, test and work on [destiny](https://github.com/Destiny-Org/destiny)
and [Fate](https://github.com/Destiny-Org/fate). Forked from the upstream D tools
repository.

The destiny and Fate builds expect this repository next to them:

```
Destiny/
├── destiny_engine/
├── fate/
├── tools/
└── d-scanner/
```

Program                | Scope    | Description
---------------------- | -------- | -----------------------------------------
catdoc                 | Build    | Concatenates Ddoc files.
checkwhitespace        | Build    | Whitespace style check used by `make style`.
ddemangle              | Public   | Symbol demangler.
detab                  | Internal | Replaces tabs with spaces.
dustmite               | Public   | [Test case minimization tool](https://github.com/CyberShadow/DustMite/wiki).
get_dlibcurl32         | Internal | Win32 libcurl downloader/converter.
rdmd                   | Public   | Build tool that compiles and runs a program in one step.
rdmd_test              | Internal | rdmd test suite.
tests_extractor        | Internal | Extracts public unittests; used by Fate. Needs libdparse from `../d-scanner`.
tolf                   | Internal | Line endings converter.
updatecopyright        | Internal | Updates the copyright notices in the compiler sources.

Report problems on the [issue tracker](https://github.com/Destiny-Org/tools/issues).

## Building

On a Posix system all tools can be built with:

```
make all
```
