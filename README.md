# Commitlint config

A shareable [commitlint](https://commitlint.js.org/) config for applications.

## Installation

[Authenticate](https://help.github.com/en/github/managing-packages-with-github-packages/configuring-npm-for-use-with-github-packages#authenticating-to-github-packages) with `npm login --registry=https://npm.pkg.github.com/` using your GitHub username and a personal access token (with the `read:packages` scope).

1. In the same directory as your `package.json` file, create or edit a `.npmrc` file to include the following line:
    ```npmrc
    @glen-84:registry=https://npm.pkg.github.com
    ```
2. Run `npm install @glen-84/commitlint-config-app --save-dev`.
3. Add `"commitlint": {"extends": ["@glen-84/commitlint-config-app"]}` to your `package.json` file.
4. Add a `commit-msg` hook with the command `npx commitlint --edit "$1"`.

## Development

### Publishing a new version

[Authenticate](https://help.github.com/en/github/managing-packages-with-github-packages/configuring-npm-for-use-with-github-packages#authenticating-to-github-packages) with `npm login --registry=https://npm.pkg.github.com/` using your GitHub username and a personal access token (with the `write:packages` scope).

1. Run `npm version patch` (replace `patch` [as necessary](https://docs.npmjs.com/cli/version)) to increase the version number.
2. Run `git push --atomic --follow-tags` to push the version commit and tag.
3. Run `npm publish` to publish the new version.

## Unused rules

### Unnecessary

* `body-empty` – body is optional.
* `footer-empty` – footer is optional.

### No use for

* `body-max-length`
* `footer-max-length`
* `references-empty`
* `scope-case`
* `scope-enum`
* `scope-max-length`
* `scope-min-length`
* `signed-off-by`
* `subject-case`
* `subject-full-stop`
* `subject-max-length`
* `subject-min-length`
* `type-case`
* `type-enum`
* `type-max-length`
* `type-min-length`
