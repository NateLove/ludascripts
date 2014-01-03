ludascripts
===========

Scripts for things that I find useful.

ludamvn
-------

A wrapper for `mvn` that provides color output.

Bugs
----

`ludamvn` doesn't handle interactive user input well. For example `ludamvn
archetype:generate` looks like it hangs, but it's just because the buffer isn't
fully flushed when the program pauses for user input.