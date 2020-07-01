# test-package

## Auto publish configuration

- install [auto](https://github.com/intuit/auto)
```shell
$ npm install -D auto
```

- create npm token at `https://www.npmjs.com/settings/<username>/tokens`
- create github token at `https://github.com/settings/tokens/new` with `repo` permissions
- make tokens available as env variables (`NPM_TOKEN`, `GH_TOKEN` on ci)

- configure ci to make auto release (full example can be seen in [.github/workflows/release.yml](.github/workflows/release.yml))
```shell
$ npx auto shipit
```

- configure auto [example](.autorc)

## Make first publish

Run npm publish --access public to create the package with public access
```shell
$ npm publish --access public
```

## Mark prs for release

One of these labels have to be added to the pr in order increment right version number after it's merged into master: `major`, `minor`, `patch`.

## Prerelease branches

This repo has `dev` prerelease branch.

## Make sure that pr contains label specifying version number to increment

see [example](.github/workflows/tag-validation.yml)
