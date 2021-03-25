# google-calendar-to-org-mode
CLI for creating an Org Mode file based on meetings in a Google Calendar

# Notes

The plan is to build using Typescript and the [oclif](https://oclif.io/docs/introduction) framework.

Also to setup Github Actions to understand the excitment.

# Developing

Using [Node Version Manager](https://github.com/nvm-sh/nvm) for managing the Node environment. Run `nvm use` to setup the environment when in the directory (it uses the `.nvmrc` file).

Need to create an OAuth project in Google Console. The secret credentials will go into the file `src/secrets.ts` which be created by copying the file `src/secrets.ts.template`. Do no checking secrets to Git!

Can override the `XDG_DATA_HOME` environment variable to change where the data file is stored. I use the following when running for local testing:

```sh
$ XDG_DATA_HOME=/tmp/store ./bin/run --backDays=1 --forwardDays=1 --port=3003 /tmp/org.org
```

# Generating native image #

Using <https://github.com/vercel/pkg> to generate the native image. Install it using:

```sh
$ npm install -g pkg
```

To build an image on MacOS run (it's slow):

```sh
pkg -t node14-macos-x64 .
```

# oclif README #

google-calendar-to-org-mode
===========================

CLI for creating an Org Mode file based on meetings in a Google Calendar

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/google-calendar-to-org-mode.svg)](https://npmjs.org/package/google-calendar-to-org-mode)
[![Downloads/week](https://img.shields.io/npm/dw/google-calendar-to-org-mode.svg)](https://npmjs.org/package/google-calendar-to-org-mode)
[![License](https://img.shields.io/npm/l/google-calendar-to-org-mode.svg)](https://github.com/oburn/google-calendar-to-org-mode/blob/master/package.json)

<!-- toc -->
* [google-calendar-to-org-mode](#google-calendar-to-org-mode)
* [Notes](#notes)
* [Developing](#developing)
* [oclif README #](#oclif-readme-)
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g google-calendar-to-org-mode
$ google-calendar-to-org-mode COMMAND
running command...
$ google-calendar-to-org-mode (-v|--version|version)
google-calendar-to-org-mode/0.0.1 darwin-x64 node-v14.15.5
$ google-calendar-to-org-mode --help [COMMAND]
USAGE
  $ google-calendar-to-org-mode COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->

<!-- commandsstop -->
