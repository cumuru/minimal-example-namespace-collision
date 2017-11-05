# What for?

This repo should demonstrate problems with PHP namespaces.

## How to install and setup?

```
git clone https://github.com/cumuru/minimal-example-namespace-collision.git
cd minimal-example-namespace-collision
composer dump-autoload
```

## What happens?

Make sure you have PHP CLI interpreters in version 5.6 and 7.1 at hand.

```
$ php7.1 index.php
success
```

```
$ php5.6 index.php
PHP Fatal error:  Cannot use Cumuru\MinimalExample\ToBeImported\Bar as Bar because the name is already in use in .../minimal-example-namespace-collision/src/Main/Foo.php on line 4
PHP Stack trace:
PHP   1. {main}() .../minimal-example-namespace-collision/index.php:0
PHP   2. spl_autoload_call() .../minimal-example-namespace-collision/index.php:6
PHP   3. Composer\Autoload\ClassLoader->loadClass() .../minimal-example-namespace-collision/index.php:6
PHP   4. Composer\Autoload\includeFile() .../minimal-example-namespace-collision/vendor/composer/ClassLoader.php:322

```