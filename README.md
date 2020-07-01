# test-package

## Auto publish configuration

- install [auto](https://github.com/intuit/auto)
```shell
$ npm install -D auto
```

- create npm token at `https://www.npmjs.com/settings/<username>/tokens`
- create github token at `https://github.com/settings/tokens/new` with `repo` permissions

## Make first publish

Run npm publish --access public to create the package with public access
```shell
$ npm publish --access public
```

## Mark prs for release

One of tese tags have to be added to the pr in order to make new release after it's merged into master: `major`, `minor`, `patch`. Given label will determine which version number will be incremented.
