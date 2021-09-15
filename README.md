<p align="center">
  <img src="https://i.imgur.com/dV1aZjJ.png" title="Taikonauten">
</p>

<h1 align="center">Taikonauten phpcs configuration</h1>

<p>&nbsp;</p>

This package provides the phpcs configuration used at [Taikonauten](https://taikonauten.com).

## Installation

First make sure [Composer](https://getcomposer.org/) is installed locally.

You may install composer using [Brew](https://brew.sh/):

```bash
brew install composer
```

Next, require the [PHP code sniffer](https://github.com/squizlabs/PHP_CodeSniffer) in your project using composer:

```bash
composer require "squizlabs/php_codesniffer=*" --ignore-platform-reqs
```

Install the main linting configuration provided by this repository using [npm](https://www.npmjs.com/):

```bash
npm install --save-dev @taikonauten/linters-phpcs
```

## Setup

Now we need to add the phpcs.xml config to the project root. There are multiple ways to do so:

### Create a local copy

You can simply copy the `phpcs.xml` provided by the `@taikonauten/linters-phpcs` package:

```bash
cp node_modules/@taikonauten/linters-phpcs/phpcs.xml phpcs.xml
```

### Symlink

Alternatively you may create a symbolic link to the config using:

```bash
ln -s node_modules/@taikonauten/linters-phpcs/phpcs.xml phpcs.xml
```

## Configuration

### Running as package.json script

Add a script to reference the local phpcs executable with our local copy of the phpcs.xml config:

```json
{
  "scripts": {
    "lint": "npm run lint:php",
    "lint:php": "./vendor/bin/phpcs --standard=phpcs.xml",
  }
}
```

By default, this will start linting all files in your project root. You might want to limit the linting to certain directories.
Do so by adding a list of directory paths as arguments:

```json
./vendor/bin/phpcs --standard=phpcs.xml web/app/themes/my-custom-theme/**/* web/app/plugins/my-custom-plugin/**/*
```

This will limit the linting to the `web/app/themes/my-custom-theme` and `web/app/plugins/my-custom-plugin` directory.

## Using with your IDE or Editor

After that, make sure your editor or IDE supports the `phpcs.xml` file.
Install a `phpcs` extension:

For [Visual Studio Code](https://code.visualstudio.com/), install the [phpcs](https://marketplace.visualstudio.com/items?itemName=ikappas.phpcs) plugin.

---

Made with ♡ at Taikonauten
