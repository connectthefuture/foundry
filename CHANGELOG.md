# foundry changelog
3.1.0 - Upgraded to `chalk@1.0.0` to resolve any instability issues via @jbnicolai in #22

3.0.1 - Added fix for `npm` for Travis CI

3.0.0 - Moved from global `node modules` to peer `node modules` for plugins

2.3.2 - Expanded `echo` test to further verify CLI/Release linkage

2.3.1 - Added another test for `release`

2.3.0 - Fixed and added test for `plugins` command

2.2.0 - Added support for `--plugin-dir` and better assertion errors for out of date plugins

2.1.0 - Added `specVersion` requirement. Fixes #20

2.0.0 - Moved from `setVersion` to `updateFiles` to match `foundry-release-spec@1.0.0`

1.1.1 - Updated `bash/zsh` completion script

1.1.0 - Improved `plugins` command output

1.0.0 - Moved to global release plugins, added `plugins` list command

0.17.1 - Added example screenshot image

0.17.0 - Updated tests to no longer test release plugins and added documentation

0.16.0 - Moved to external `pypi` release plugins

0.15.0 - Upgraded to `foundry-release-git@1.0.0` and supporting `foundry-release-spec@0.2.0` via `commit` step

0.14.0 - Moved to external `bower` and `component` release plugins

0.13.0 - Moved to external `git` release plugin

0.12.0 - Introduced `glob` discovered modules

0.11.0 - Relocated `message` generation from `git` plugin to `release` command itself

0.10.0 - Moved from `version` to `params` for all release steps

0.9.0 - Broke up setVersion, register, and publish into release specific libraries

0.8.1 - Corrected lint errors

0.8.0 - Moved from minified `exec` calls to update version to `fs` read/write

0.7.0 - Rearranged steps into setVersion, register, and publish

0.6.0 - Relocated foundry library from `bin` to `lib`

0.5.0 - Upgraded completion library to `commander-completion`

0.4.1 - Removed extra space from auto-complete output

0.4.0 - Added rudimentary bash/zsh completion via opt-in `npm run link-bash-completion`

0.3.0 - Completed tests for `release-bower`, `release-component`, and `release-pypi`

0.2.0 - Refactored Factory to extend from Commander and started `release-npm` test

0.1.2 - Fixed git test in Travis CI

0.1.1 - Updated test to run against `git` and in enclosed environments only

0.1.0 - Initial port of `git-release` hooks from `twolfson/dotfiles`
