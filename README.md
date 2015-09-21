# eslint-config-shopify

This package provides Shopify's `.eslintrc` as an extensible shared config.

## Usage

### React

Install this module, as well as the other eslint modules on which it is dependent:

```shell
npm install --save-dev eslint babel-eslint eslint-plugin-react eslint-plugin-shopify # dependencies
npm install --save-dev eslint-config-shopify
```

then, extend the React version of this configuration in your own `.eslintrc`:

```json
{
  "extends": "shopify/react"
}
```

### ES2015 and Beyond Projects

Install this module, as well as the other eslint modules on which it is dependent:

```shell
npm install --save-dev eslint babel-eslint eslint-plugin-shopify # dependencies
npm install --save-dev eslint-config-shopify
```

then, extend the base version of this configuration in your own `.eslintrc`:

```json
{
  "extends": "shopify"
}
```

### ES5 Projects

Projects with a legacy codebase or that target a tool that targets node may continue to use ES5. To lint these projects, first install this module, as well as the other eslint modules on which it is dependent:

```shell
npm install --save-dev eslint eslint-plugin-shopify # dependencies
npm install --save-dev eslint-config-shopify
```

then, extend the ES5 version of this configuration in your own `.eslintrc`:

```json
{
  "extends": "shopify/es5"
}
```

## Contributing

If there are rules that you wish to alter for your particular project, feel free to do so in your own `.eslintrc`. Rule declarations you make there will override the rules declared by this configuration. If you feel that a particular rule choice is poor and should be changed for all projects using this configuration, please open a PR [against this repo on Github](https://github.com/Shopify/eslint-config-shopify).

For changes to existing rules, bump the major version. For addition of new rules, bump the minor version. For all other corrections and updates, bump the patch version. These can easily be done by running `npm publish <version>`, where `version` is either `major`, `minor`, or `patch`.

## Changelog

### 5.2.0

Added the Shopify plugin and initial rule defaults.

### 5.1.0

Added an ES5 version of the config.

Added a few minor exceptions to the `id-length` rule.

### 5.0.0

Prevent implicit coercions.

### 4.0.0

Force `let` in all cases. `const` is allowed but not enforced (use it sparingly to indicate immutable primitives).

Force function declarations (`function foo() {}`) over function expressions (`var foo = function() {}`).

Force variable initialization at definition (i.e., no `let foo;`, must be assigned).

Force parens for arrow function parameters regardless of arity, and force spaces around the actual arrow.

Prefer template strings over concatenation, and spread (`...`) over `.apply()`.

Other minor rule additions and updates.

### 3.0.4

Allow function declarations to be used before defined (avoids issues with, for example, functions that call each other recursively).

### 3.0.3

Avoid escape in quote styles.

### 3.0.2

Forgot to bump to package.json version.

### 3.0.1

Use jsx-quotes instead of react/jsx-quotes.

### 3.0.0

Enforce trailing commas on multiline literals.

Enforce double quotes for JSX to be in line with XML.

Don't allow spacing inside object literals.

### 2.0.1

Fixed typo in one rule. Minor project cleanup.

### 2.0.0

All warnings are now errors. Removed some rules relating to complexity, maximum length, and nesting depth.

### 1.0.7

Loosens restriction on `==` for `null` checking (which Flow requires for Maybe types).

### 1.0.6

Adds global Flow types for React (`ReactClass` and `ReactElement`).

### 1.0.5

Prefer `var` until Flow adds support for `const`/ `let`.

### 1.0.4

Allow `continue`

### 1.0.3

Prefer `const`/ `let`.

### 1.0.2

Updated React linting rules.

### 1.0.1

Removed unnecessary dependencies.

### 1.0.0

Initial commit.
