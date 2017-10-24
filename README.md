[![Build Status](https://img.shields.io/travis/seek-oss/eslint-config-sku/master.svg?style=flat-square)](http://travis-ci.org/seek-oss/eslint-config-sku) [![npm](https://img.shields.io/npm/v/eslint-config-sku.svg?style=flat-square)](https://www.npmjs.com/package/eslint-config-sku) [![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg?style=flat-square)](https://github.com/semantic-release/semantic-release) [![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg?style=flat-square)](http://commitizen.github.io/cz-cli/)


# eslint-config-sku

This package includes the shareable ESLint configuration used by [sku](https://github.com/seek-oss/sku).

## Usage in sku Projects

The easiest way to use this configuration is with [sku](https://github.com/seek-oss/sku), which includes it by default.

**You don’t need to install it separately in sku projects.**

## Usage Outside of sku

If you want to use this ESLint configuration in a project not built with sku, you can install it with following steps.

First, install this package, ESLint and the necessary plugins listed in this project's [package.json](package.json).

Then create a file named `.eslintrc` with following contents in the root folder of your project:

```js
{
  "extends": "sku"
}
```

You can override the settings from `eslint-config-sku` by editing the `.eslintrc` file. Learn more about [configuring ESLint](http://eslint.org/docs/user-guide/configuring) on the ESLint website.

## sku/unpretty

The core sku config does not include formatting concerns.  
It is recommended to use [Prettier](https://www.npmjs.com/package/prettier) to lint formatting concerns.  
If you are not using Prettier and would like to enable formatting rules, use `sku/unpretty` in addition to the core `sku` config.  

```js
{
  "extends": ["sku", "sku/unpretty"]
}
```

## License

MIT.
