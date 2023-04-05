# PhpSpreadsheet

PhpSpreadsheet-classera is a fork for PhpOffice/PhpSpreadsheet, this fork was made in order to match our classera code without any edit in the project code after the deprecation of PHPExcel.

## PHP Version Support

LTS: Support for PHP versions will only be maintained for a period of six months beyond the
[end of life](https://www.php.net/supported-versions) of that PHP version.

Currently the required PHP minimum version is PHP __7.4__, and we [will support that version](https://www.php.net/eol.php) until 28th June 2023.

See the `composer.json` for other requirements.

## Installation

Use [composer](https://getcomposer.org) to install PhpSpreadsheet into your project:

```sh
composer require abuel3abbas/phpspreadsheet-classera
```

If you are building your installation on a development machine that is on a different PHP version to the server where it will be deployed, or if your PHP CLI version is not the same as your run-time such as `php-fpm` or Apache's `mod_php`, then you might want to add the following to your `composer.json` before installing:
```json
{
    "require": {
        "abuel3abbas/phpspreadsheet-classera": "^1.0"
    },
    "config": {
        "platform": {
            "php": "7.4"
        }
    }
}
```
and then run
```sh
composer install
```
to ensure that the correct dependencies are retrieved to match your deployment environment.

See [CLI vs Application run-time](https://php.watch/articles/composer-platform-check) for more details.


One or the other of these libraries is necessary if you want to generate HTML or PDF files that include charts; or to render a Chart to an Image format from within your code.
They are not necessary to define charts for writing to `Xlsx` files.
Other file formats don't support writing Charts.

## Documentation

Read more about it, including install instructions, in the [official documentation](https://phpspreadsheet.readthedocs.io). Or check out the [API documentation](https://phpoffice.github.io/PhpSpreadsheet).

Please ask your support questions on [StackOverflow](https://stackoverflow.com/questions/tagged/phpspreadsheet), or have a quick chat on [Gitter](https://gitter.im/PHPOffice/PhpSpreadsheet).


## PHPExcel vs PhpSpreadsheet ?

PhpSpreadsheet is the next version of PHPExcel. It breaks compatibility to dramatically improve the code base quality (namespaces, PSR compliance, use of latest PHP language features, etc.).

Because all efforts have shifted to PhpSpreadsheet, PHPExcel will no longer be maintained. All contributions for PHPExcel, patches and new features, should target PhpSpreadsheet `master` branch.

Do you need to migrate? There is [an automated tool](/docs/topics/migration-from-PHPExcel.md) for that.

## Migration

The main purpose of this repo is to migrate to phpoffice/spreadsheet with the least amount of changes so we edited the classes alises in composer.json to matchup the the classes names in phpexcel, I used a guide to do that with chatgpt here is the guide link :
https://phpspreadsheet.readthedocs.io/en/latest/topics/migration-from-PHPExcel/


