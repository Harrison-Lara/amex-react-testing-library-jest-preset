> An opinionated [Jest preset](http://facebook.github.io/jest/docs/en/configuration.html#preset-string) for React modules.
> <br />
> For non-React projects use [amex-jest-preset](https://github.com/americanexpress/amex-jest-preset)<br />
> For React Enzyme projects use [amex-jest-preset-react](https://github.com/americanexpress/amex-jest-preset-react)

## ๐ฉโ๐ป Hiring ๐จโ๐ป

> Want to get paid for your contributions to `amex-react-testing-library-jest-preset`?
> Send your resume to oneamex.careers@aexp.com

## ๐ Table of Contents

- [Features](#-features)
- [Usage](#-usage)
- [API](#%EF%B8%8F-api)
- [License](#%EF%B8%8F-license)
- [Code Of Conduct](#%EF%B8%8F-code-of-conduct)
- [Contributing](#-contributing)

## โจ Features

- Base for Jest React Testing Library configuration for React modules

## ๐คนโ Usage

1. Install:

   ```bash
   npm install --save-dev amex-react-testing-library-jest-preset
   ```

2. And in your [Jest configuration][]:

   ```json
   {
     "preset": "amex-react-testing-library-jest-preset"
   }
   ```

And... that's it! You now have all the boilerplate Jest configurations set up for you! Running `jest` from your `npm test` script will use all these configurations!

## ๐๏ธ API

### Extending the preset provided configuration

You can add on and/or override any values provided in this preset as you wish in your [Jest configuration][].

It should be noted that if overriding the `setupFilesAfterEnv` option you may want to extend off of the [setup file provided by amex-react-testing-library-jest-preset](./jest-setup.js) in order to preserve that files' content. Otherwise you will lose anything we provide for you in [there](./jest-setup.js). Do so as follows:

```javascript
// in custom-jest-setup.js
require('amex-react-testing-library-jest-preset/jest-setup');

// your own custom setup
```

### Configurations

Extends [amex-jest-preset](https://github.com/americanexpress/amex-jest-preset) and adds the following configurations that are specific to testing React modules:

- [testEnvironment](https://testing-library.com/docs/react-testing-library/setup#jest-27) tells Jest to use `jest-environment-jsdom` test environment as it is often used while testing React components ([amex-jest-preset](https://github.com/americanexpress/amex-jest-preset) sets `testEnvironment` to `node`)

- [moduleNameMapper](http://facebook.github.io/jest/docs/en/configuration.html#modulenamemapper-object-string-string) tells Jest to treat CSS modules as identity objects

- [setupFilesAfterEnv](https://jestjs.io/docs/en/configuration.html#setupfilesafterenv-array) is where we setup [React Testing Library](https://testing-library.com/docs/react-testing-library/setup)

- [snapshotSerializers](http://facebook.github.io/jest/docs/en/configuration.html#snapshotserializers-array-string) tells Jest to use [jest-serializer-html](https://github.com/algolia/jest-serializer-html#readme) serializer

### Compatibility

This package is compatible only with React 16+.

## ๐๏ธ License

Any contributions made under this project will be governed by the [Apache License
2.0](./LICENSE.txt).

## ๐ฃ๏ธ Code of Conduct

This project adheres to the [American Express Community Guidelines](./CODE_OF_CONDUCT.md).
By participating, you are expected to honor these guidelines.

[jest configuration]: http://facebook.github.io/jest/docs/en/configuration.html

## ๐ Contributing

We welcome Your interest in the American Express Open Source Community on Github.
Any Contributor to any Open Source Project managed by the American Express Open
Source Community must accept and sign an Agreement indicating agreement to the
terms below. Except for the rights granted in this Agreement to American Express
and to recipients of software distributed by American Express, You reserve all
right, title, and interest, if any, in and to Your Contributions. Please [fill
out the Agreement](https://cla-assistant.io/americanexpress/).

Please feel free to open pull requests and see [CONTRIBUTING.md](./CONTRIBUTING.md) to learn how to get started contributing.
