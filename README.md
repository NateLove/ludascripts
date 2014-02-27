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

Quickly delpoy an exploded WAR to a local server by creating a symlink from the
server's deployments folder to the current folder (which must be your project's
exploded WAR).

Currently handles JBoss and Tomcat correctly. Examples: `ldeploy jboss` (deploy
the current exploded WAR to JBoss), `ldeploy tomcat` (same, but to Tomcat),
`ldeploy jboss clean` (remove all deployments from JBoss), `ldeploy tomcat
clean` (remove all custom deployments from Tomcat without removing the standard
deployments that come bundled with Tomcat).

Bugs
----

`lmvn` doesn't handle interactive user input well because it buffers output to
colorize it. For example `lmvn archetype:generate` looks like it hangs, but it's
just because the buffer isn't fully flushed when the program pauses for user
input. This could be fixed by using a lower-level coloring scheme instead of
buffering the maven output.