<p align="center">
  <img src="https://i.imgur.com/dV1aZjJ.png" title="Taikonauten">
</p>

<h1 align="center">Taikonauten phpcs configuration</h1>

<p>&nbsp;</p>

This package provides the phpcs configuration used at [Taikonauten](https://taikonauten.com).

## Installation

```bash
brew install composer
```

```bash
composer global require "squizlabs/php_codesniffer=*" --ignore-platform-reqs
```

Inside project root

```bash
npm install --save-dev @taikonauten/linters-phpcs
```

```bash
ln -s node_modules/@taikonauten/linters-phpcs/phpcs.xml phpcs.xml
```

## Using with your IDE or Editor

After that, make sure your editor or IDE supports the `phpcs.xml` file.
Install a `phpcs` extension:

For [Visual Studio Code](https://code.visualstudio.com/), install the [phpcs](https://marketplace.visualstudio.com/items?itemName=ikappas.phpcs) plugin.

---

Made with ♡ at Taikonauten
