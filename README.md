# @cyansalt/tsconfig

[![npm](https://img.shields.io/npm/v/@cyansalt/tsconfig.svg)](https://www.npmjs.com/package/@cyansalt/tsconfig)

My TypeScript configuration.

## Installation

```shell
npm install --save-dev @cyansalt/tsconfig
```

## Usage

```json5
// tsconfig.json
{
  "extends": "@cyansalt/tsconfig/tsconfig.app"
  // OR in short (not recommended)
  // "extends": "@cyansalt/tsconfig"
}
```

For base libraries (which will be used as dependencies):

```json5
// tsconfig.json
{
  "extends": "@cyansalt/tsconfig/tsconfig.lib"
}
```

By default, tsc will not output any files when using the above configuration. The following configuration may be additionally required:

```json5
// tsconfig.json
{
  "compilerOptions": {
    // To emit .js files when compiling
    "noEmit": false,
    // To emit .d.ts files when compiling
    "declaration": true
  }
}
```

In addition, you will also need to specify the files to be included (`include`) or excluded (`exclude`) yourself.

For more information, see [TSConfig](https://www.typescriptlang.org/tsconfig/).
