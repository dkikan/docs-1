---
title: "Automated Testing"
categories: ["testing"]
tags: []
weight: 80
contributors: ["skuipers"]
---

Gibbon uses [PHPUnit](https://phpunit.de/) and [Codeception](https://codeception.com/) for automated testing, introduced in v14.0.00. Both testing frameworks can be installed and configured to run in your localhost.

> Note: Our refactoring efforts are ongoing, and the code coverage for automated tests is not all-encompassing. A passing test does not guarantee a working codebase: please always test manually too.

### PHPUnit ###
PHPUnit tests can be run with the `phpunit .` command in the /tests folder
If you have downloaded phpunit as .phar then use the following command from within the /tests folder
> php <path to phpunit.phar> .
  e.g., php ..\..\phpunit-9.5.28.phar .
If for some reason php is not recognized as a valid command then please add path to php.exe in the environment settings in windows or similar setting in linux based system
  e.g., PATH=%PATH%;C:\wamp64\bin\php\php8.0.13
  
### Codeception ###
Codeception tests can be run with the `codecept run` command in the /tests folder

Codeception involves integration testing and makes use of a database connection; it will not run unless explicitly enabled. To enable Codeception testing in Gibbon, add the following to your config.php file:

```php
$testEnvironment = 'codeception';
```

### Travis CI ###

Pull requests and commits to the development branch are automatically built & tested using [Travis CI](https://travis-ci.org/GibbonEdu/core).
