# V
[V] (https://github.com/rupa/v) is a tool to fast open recently edited files using vim.

## Installation

Quite simple, just put the `v` command file to some directory under `$PATH` environment variable(`/usr/local/bin` for example).

## Usage

```
v foo bar
```
Open the most recently used file matching 'foo' and 'bar' (that is, both 'foo' and 'bar' are part of full file path).

```
v -l foo
```
The `-l` option is specified to list all items matched, rather than open the most match.

```
v -c foo
```
The `-c' option restrict matches to subdirectories of the current dir
