# WPCS-Lint-Fix

A set of configuration files to lint and fix your files according to WordPress Coding Standards.

## Installation

Download all the files in this repository and place them in the root directory of your project (theme, plugin...).

If your project already contains a composer.json or a package.json file, please check the packages to install them manually (either by copying the contents of the file or by command line).

## Usage

Open the _phpcs.xml.dist_ file and replace "_yourPrefix_" and "_yourTextDomain_".

### Composer

Make sure [Composer](https://getcomposer.org/) is installed on your system. Then:

```
composer install
```

Running this command will:

1. Install PHP_CodeSniffer.
2. Install WordPress standards.
3. Register WordPress standards in PHP_CodeSniffer configuration.
4. Make `phpcs` and `phpcbf` commands available.

Two scripts are configured in the _composer.json_ file:

-   `wplint`: lint with `phpcs` according to WordPress standards.
-   `wpfix`: fix with `phpcbf` according to WordPress standards.

**Examples:**

```
composer wpfix .
```

This command will attempt to correct the problems in all your files.

```
composer wpfix /path/to/your/file.ext
```

This command will attempt to correct the problems in the specified file.

Some errors cannot be fixed by `phpcbf`, but your text editor should inform you of the remaining problems in your files.

### npm

Make sure [npm](https://www.npmjs.com/) is installed on your system. Then:

```
npm install
```

Running this command will:

1. Install Prettier.
2. Install ESLint.
3. Install ESLint plugin for WordPress development.
4. Install Stylelint.
5. Install Stylelint rules for WordPress develpment.

## In addition

A folder specific to VSCode is present in this repository. It contains some settings that I use for my WordPress projects. The extensions used are:

-   [phpcs](https://marketplace.visualstudio.com/items?itemName=ikappas.phpcs)
-   [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

## Disclaimer

I use this as base for my projects (themes and plugins). I can't guarantee 100% adherence to the official [WordPress Coding Standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/).
