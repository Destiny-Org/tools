# Destiny tools

Tools used to build, test and work on [destiny](https://github.com/Destiny-Org/destiny)
and [Fate](https://github.com/Destiny-Org/fate). Forked from the upstream D tools
repository.

The destiny and Fate builds expect this repository next to them:

```
Destiny/
├── destiny_engine/
├── fate/
└── tools/
```

Program                | Scope    | Description
---------------------- | -------- | -----------------------------------------
catdoc                 | Build    | Concatenates Ddoc files.
changed                | Internal | Change log generator (still queries upstream D trackers).
checkwhitespace        | Build    | Whitespace style check used by `make style`.
ddemangle              | Public   | Symbol demangler.
detab                  | Internal | Replaces tabs with spaces.
dget                   | Internal | Source code downloader.
dman                   | Public   | Documentation lookup tool.
dustmite               | Public   | [Test case minimization tool](https://github.com/CyberShadow/DustMite/wiki).
get_dlibcurl32         | Internal | Win32 libcurl downloader/converter.
rdmd                   | Public   | Build tool that compiles and runs a program in one step.
rdmd_test              | Internal | rdmd test suite.
tests_extractor        | Internal | Extracts public unittests (requires DUB); used by Fate.
tolf                   | Internal | Line endings converter.
updatecopyright        | Internal | Updates the copyright notices in the compiler sources.

Report problems on the [issue tracker](https://github.com/Destiny-Org/tools/issues).

## Building

On a Posix system all tools can be built with:

```
make all
```

## Using DUB as a build tool

Most tools can also be built with DUB:

```
dub build :ddemangle
```

Some tools require the DUB package manager. On a Posix system, their source
files can be run directly (for example `./tests_extractor.d`), or with:

```
dub --single tests_extractor.d
```

Pass `--` before the program's arguments, for example
`dub --single tests_extractor.d -- -i ../fate/std/algorithm`.
