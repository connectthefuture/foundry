# foundry [![Build status](https://travis-ci.org/twolfson/foundry.png?branch=master)](https://travis-ci.org/twolfson/foundry)

Release manager for [npm][], [bower][], [component][], [PyPI][], [git tags][], and any plugin you can write.

[npm]: http://npmjs.org/
[bower]: http://bower.io/
[component]: http://component.io/
[PyPI]: http://pypi.python.org/
[git tags]: http://git-scm.com/

This was created out of frustration; there was no generic *sharable* release manager. Previously, I was using [git-extra's git-release][] command with [dotfiles git hooks][].

[git-extra's git-release]: https://github.com/visionmedia/git-extras/blob/1.9.0/Readme.md#git-release
[dotfiles git hooks]: https://github.com/twolfson/dotfiles/tree/0.39.1/git-template-dir/hooks

// TODO: Example output (probably via screenshot)

## Getting Started
Install the module globally via: `npm install -g foundry`

Once installed, you can run a release in any package you own. The current built-in plugins are `git`, `npm`, `bower`, `component`, and `PyPI`.

> In `1.0.0`, we will remove the built-in release libraries. This means you will need to globally install the release libraries you want.

For example purposes, we will create/release on a local-only `git` repository.

```bash
# Create git repo
mkdir foundry-example
cd foundry-example
git init
echo "Hello World" > README.md
git add README.md
git commit -m "Added documentation"

# Run our release
foundry release
# [master c6ce921] Release 0.1.0

# See the release commit and tag
git log --decorate --oneline
# c6ce921 (HEAD, tag: 0.1.0, master) Release 0.1.0
# f0c25b3 Added documentation
```

## Documentation
`foundry` provides a command line interface for releasing.

```bash
$ foundry --help

  Usage: foundry [options] [command]

  Commands:

    release <version>      Set version for package metadata and publish to registries
    completion             Get potential completions for a command. Looks for `COMP_CWORD`, `COMP_LINE`, `COMP_POINT`.

  Options:

    -h, --help     output usage information
    -V, --version  output the version number

```

Example releases are:

```bash
foundry release 0.1.0
foundry release 0.3.0
foundry release 1.0.0
```

> It is planned to allow for `foundry release major`, `foundry release minor`. See https://github.com/twolfson/foundry/issues/16

### Process

When a release occurs, the following steps are processed:

1. Set version, update package metadata with the new version (e.g. update `package.json`)
2. Commit, persist any changes to a version control system (e.g. `git commit && git tag`)
3. Register, if the package is brand new (semver === `0.1.0`), then register it to its repository (e.g. `python setup.py register`)
4. Publish, release changes to package's repostiroy manager (e.g. `npm publish`)


## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint via [grunt](https://github.com/gruntjs/grunt) and test via `npm test`.

## Donating
Support this project and [others by twolfson][gittip] via [gittip][].

[![Support via Gittip][gittip-badge]][gittip]

[gittip-badge]: https://rawgithub.com/twolfson/gittip-badge/master/dist/gittip.png
[gittip]: https://www.gittip.com/twolfson/

## Unlicense
As of Dec 07 2013, Todd Wolfson has released this repository and its contents to the public domain.

It has been released under the [UNLICENSE][].

[UNLICENSE]: UNLICENSE
