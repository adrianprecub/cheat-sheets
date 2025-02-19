---
title: npm
createdDate: 2017-05-19
updatedDate: 2019-03-01
published: true
---

A list of terminal commands and flags to help me use `npm`

## install package.json dependencies

```bash
npm install
```

**Shorthand**

```bash
# install
npm i <package>
# uninstall
npm un <package>
# update
npm up <package>
```

## List globally installed packages.

```bash
npm list -g --depth=0
```

## list available scripts to run

```bash
npm run
```

## update npm

```bash
npm install -g npm@latest
# using windows? Then use
npm-windows-upgrade
```

## flags

`-S` is the same as `--save` not needed in npm 5 `-D` is the same as
`--save-dev`

## installed version

```bash
npm list # for local packages
```

## Node Version Manager `nvm`

Say you want to install Node v6.9.1 you would write on the terminal:

```bash
nvm install 6
```

If you have multiple versions of Node.js installed on your workspace,
you can switch to a specific version by writing:

```bash
nvm use 0.10.40
```

Making a node version default

In order to set a default version of node for your workspace, just
type:

```bash
nvm alias default 6
```

Where 6 was the version you wanted to be used as default.

## Uninstall global package

```bash
npm -g uninstall <name> --save
```

## Upgrade NPM on Windows

After trying several times to upgrade npm on Windows I found this
whilst poking around.

```bash
npm-windows-upgrade
```

## Updating global packages

To update global packages individually you can use:

```bash
npm update -g <package>
```

To see which packages need updating use:

```bash
npm outdated -g --depth=0
```

## npx, one off command

No need to install create react app if you don't want to

```bash
npx create-react-app my-new-app
```

Will use latest create react app to make your new app

## update all project dependencies

Update dependencies with `npm-check`

```bash
npx npm-check -u
```

## dont `rm -rf node_modules; npm install`

Instead use:

```bash
npm ci
```

It will have the same effect but be 2-3x faster 👌
