ludascripts
===========

Scripts for things that I find useful.

lmvn
-------

A wrapper for `mvn` that provides color output. This is especially useful for
tests, since you can just skim the test output for red to see which tests
failed.

ldepoly
-------

Quickly delpoy a web project to a local server by creating a symlink from the
server's deployments folder to the current folder (which must be your project's
exploded WAR).

Bugs
----

`lmvn` doesn't handle interactive user input well because it buffers output to
colorize it. For example `lmvn archetype:generate` looks like it hangs, but it's
just because the buffer isn't fully flushed when the program pauses for user
input. This could be fixed by using a lower-level coloring scheme instead of
buffering the maven output.