---
title: npm-test
section: 1
description: Test a package
github_repo: npm/cli
github_branch: latest
github_path: docs/lib/content/commands/npm-test.md
redirect_from:
  - /cli-documentation/v9/cli-commands/npm-test
  - /cli-documentation/v9/cli-commands/test
  - /cli-documentation/v9/commands/npm-test
  - /cli-documentation/v9/commands/test
  - /cli-documentation/v9/npm-test
  - /cli-documentation/v9/test
  - /cli/v9/cli-commands/npm-test
  - /cli/v9/cli-commands/test
  - /cli/v9/commands/test
  - /cli/v9/npm-test
  - /cli/v9/test
---

### Synopsis

```bash
npm test [-- <args>]

aliases: tst, t
```

### Description

This runs a predefined command specified in the `"test"` property of
a package's `"scripts"` object.

### Example

```json
{
  "scripts": {
    "test": "node test.js"
  }
}
```

```bash
npm test
> npm@x.x.x test
> node test.js

(test.js output would be here)
```

### Configuration

#### `ignore-scripts`

* Default: false
* Type: Boolean

If true, npm does not run scripts specified in package.json files.

Note that commands explicitly intended to run a particular script, such as
`npm start`, `npm stop`, `npm restart`, `npm test`, and `npm run-script`
will still run their intended script if `ignore-scripts` is set, but they
will *not* run any pre- or post-scripts.

#### `script-shell`

* Default: '/bin/sh' on POSIX systems, 'cmd.exe' on Windows
* Type: null or String

The shell to use for scripts run with the `npm exec`, `npm run` and `npm
init <package-spec>` commands.

### See Also

* [npm run-script](/cli/v9/commands/npm-run-script)
* [npm scripts](/cli/v9/using-npm/scripts)
* [npm start](/cli/v9/commands/npm-start)
* [npm restart](/cli/v9/commands/npm-restart)
* [npm stop](/cli/v9/commands/npm-stop)
