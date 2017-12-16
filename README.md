# natsort

## Introduction

Natural sorting is something that can be really useful in \*nix shell
programming.  If you've ever used `ls -1v`, you've used natural sorting.

Sometimes this type of sorting is needed when `ls` can't be used (e.g., when
lines within a file need to be sorted in this special way).  This script
solves this problem by providing a more generic interface to the feature.

See the official [PHP documentation](https://secure.php.net/manual/en/function.natsort.php)
on the `natsort()` function.  You will find a description of why this tool
is useful along with a discussion of its limitations.

## Function

The syntax for the invocation of the `natsort` script is as follows:

```
natsort [-i] [-r] [--] [FILE, ...]
```

Each file argument is read into memory, and the collection of lines is
sorted before being printed to the standard output.  If no arguments are
specified, the lines to be sorted are read from the standard input.

The allowed options are:

* `-i` ignores case
* `-r` reverses the sort order
* `--` signals the end of options, remaining arguments are files

I've found the `-i` option to be particularly useful.

## Suggested Use

When a use case is encountered that requires this utility, it will be quite
obvious.  This script was written because I grew tired of repeatedly hacking
together a solution when this type of sorting was needed.

Use it through your editor or on the command line.  It's clean and
surprisingly helpful for such a simple script.
