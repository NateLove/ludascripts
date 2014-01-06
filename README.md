ludascripts
===========

Scripts for things that I find useful.

lmvn
-------

A wrapper for `mvn` that provides color output. This is especially useful for
tests, since you can just skim the test output for red to see which tests
failed.

jdepoly
-------

Quickly delpoy a web project to JBoss by creating a symlink from your
JBOSS_HOME/standalone/deployments folder to your current project's exploded WAR.

Bugs
----

`lmvn` doesn't handle interactive user input well. For example `lmvn
archetype:generate` looks like it hangs, but it's just because the buffer isn't
fully flushed when the program pauses for user input. This could be fixed by
using a lower-level coloring scheme instead of buffering the maven output.