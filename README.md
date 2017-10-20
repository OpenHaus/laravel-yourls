# laravel-yourls
Shorten urls from Laravel using your custom YOURLS.org server

## Installation

Require this package with composer.

```shell
composer require orumad/laravel-yourls
```

Laravel 5.5 automagically discovers packages so it is not required to manually add the ServiceProvider.

> If you use a catch-all/fallback route, make sure you load the Debugbar ServiceProvider before your own App ServiceProviders.

### Laravel 5.5+:

Without auto-discovery add the ServiceProvider to the providers array in config/app.php

```php
Orumad\Yourls\YourlsServiceProvider::class,
```

If you want to use the facade to log messages, add this to your facades in app.php:

```php
'Yourls' => Orumad\Yourls\YourlsFacade::class,