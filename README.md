gitstory
========

Show the commit history for a given file, after applying user-specified options to `git log`.

I built this for when I'm trying to learn the "why" for a change,
and I want to see the "narrative" of the file.
If I want to see everything that touched line 10 of something,
I'd say `gitstory -l 10 path/to/file`.
Or a range works too: `gitstory -l 10,20 path/to/file`.
This is a lot like `git -L 10,20:filename`
except the diffs include *all* changes to the file from each commit.


Usage
-----

    gitstory [log options] <filename>



Bugs and Known Issues
---------------------

- It would be nice to get the whole thing in an automatic pager like other git commands.
  If I added `--color` arguments to the git command in the loop you could say
  `gitstory ... | less -R`.
  But what I should do is detect if I'm outputting to a terminal,
  and if so do that for you automatically.

- It seems like it'd be nicer if this were `git story` instead of `gitstory`,
  but I don't see how to make a git alias run shell commands.


Copyright
---------

Copyright (c) 2018 Paul A. Jungwirth.
See LICENSE.txt for further details.

