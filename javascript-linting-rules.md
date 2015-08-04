**[⬅ Back to Coding Culture](README.md)**

# Javascript Linting Rules

The following rules should be applied to all of our javascript projects.

If a rule is absent from rule set below, please adhere to the conventions used in the current project.

_A project may use additional rules to ones listed here, but these would not be part of the current standard and such
rules are subject to change in the future._

## Current Rules

These are stored in the [linters](https://raw.githubusercontent.com/doinginc/culture/master/linters) folder in this repository.

For an explanation of these rules please refer to the [JSHint documentation](http://jshint.com/docs/options/).

## Implementation

### Adding to your project

Add the .editorconfig, .jshintrc & .jshintrcignore files from the [linters](https://raw.githubusercontent.com/doinginc/culture/master/linters) folder to the root of your project.

Then run the following commands to add jshint to your package.json file:

#### Node Linting

```bash
npm install jshint --save-dev
npm install jshint-stylish --save-dev
```

Then you can run the following command to test linting:

```bash
./node_modules/jshint/bin/jshint --reporter=node_modules/jshint-stylish ./path/to/js
```

You can then add it to your package.json file like so:

```js
{
  "scripts": {
    "lint": "./node_modules/jshint/bin/jshint --reporter=node_modules/jshint-stylish" ./path/to/js
  }
}
```

which will allow you to run:

```bash
npm run lint
```

#### Grunt Linting

```bash
npm install grunt-contrib-jshint --save-dev
npm install jshint-stylish --save-dev
```

you could have a grunt command that looks like this:

```js
module.exports = {
	dist: [
		'www/src/js/*.js',
		'www/src/js/**/*.js',
		'test/*.js'
	],
	options: {
		jshintrc: '.jshintrc',
		reporter: require('jshint-stylish')
	}
};
```

Then you can run the following command to test linting:

```bash
grunt jshint:dist
```

You can then add it to your package.json file like so:

```js
{
  "scripts": {
    "lint": "grunt jshint:dist"
  }
}
```

which will allow you to run:

```bash
npm run lint
```

## Expanding current rules

In order for a rule to be added to the above list it requires the following:

1. A valid reason for adoption the rule.
1. Agreement from the Lead Software Engineer
