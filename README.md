ssf - Simple Stream Finder
==========================

Tool for quick and efficent retrieval of parts from huge files.

Usage:
`ssf input_file --search= --limit=`
Example:
`ssf file.xml --search="<object id='123'" --limit="</object>"`
This example will return any string between "<object id='123'" and
"</object>" from the file file.xml.

Flags
=====

* `-i` => case insensitive search
* `-g` => returns all matches, not only first
* `-v` => write progress to stderr
* `-b` => buffered output: will be returned only when `--limit` is hit
* `-e` => when exists EOF reaching will be returned to stderr

Options
=======

* `--bufflen=` => Enabled buffered output, but instead of printing output when
`--limit` is hit it prints it after given amount of aggregated bytes
* `--attempt-format=` => with values: `json`, `xml`, `serialized` allows to
format before printing the aggregated data unit (understood as the text between
`--start` and `--limit` [including them]); a chain of formatters can be provided
for example: `--attempt-format=xml,json`. If none of the formatters will succeed
then plain output is returned

TODO
====

- regex support

CONTRIBUTION
============

Just do a Pull Request and we shall talk about it :)
