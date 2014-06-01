gramcheck
=========

Help make anagram poems.

Setup
-----

$ git clone git@github.com:douglasnaphas/gramcheck.git gramcheck
$ cd gramcheck
$ make # deploys to /usr/bin
$ gramcheck FILE # Check whether lines in FILE are anagrams of the first line.

Usage
-----
gramcheck [OPTIONS] [FILE]: Say whether the lines above the separator "====" are anagrams of the first line of FILE.

Report on all lines if "====" never appears. Ignore everything between "//" and newline, empty lines, and lines with no letters.

OPTIONS
-h --help
	Display this help and exit.

EXAMPLES
$ cat Tobey\ Ward
Tobey Ward

Toy bed war!
Boy we dart // Change this one
to bed wary.

// Add more.

====

tobey ward

draw
bot
draw ye bot
obey
toward bey
$ gramcheck Tobey\ Ward # Check whether the first 4 lines are anagrams of each other.
