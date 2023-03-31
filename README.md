<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

## Database Snapshot
##### To create a snapshot (which is just a dump from the database) run:
```php
php artisan snapshot:create my-first-dump
```
Giving your snapshot a name is optional. If you don't pass a name the current date time will be used

##### Snapshot a couple of tables:
```php
php artisan snapshot:create --table=posts,users
```

##### Create compressed snapshots:
```php
php artisan snapshot:create my-compressed-dump --compress
```
##### To load a previous dump issue this command:
```php
php artisan snapshot:load my-first-dump
```
##### To load a previous dump to another DB connection:
```php
php artisan snapshot:load my-first-dump --connection=connectionName
```
##### By default, snapshot:load will drop all existing tables in the database. If you don't want this behaviour, you can pass the --drop-tables=0 option:
```php
php artisan snapshot:load my-first-dump --drop-tables=0
```

##### By default, snapshot:load will load the entire snapshot into memory which may cause problems when using large files. To avoid this, you can pass the --stream option to stream the snapshot to the database one statement at a time:
```php
php artisan snapshot:load my-first-dump --stream
```

##### To list all the dumps run:
```php
php artisan snapshot:list
```

##### A dump can be deleted with:
```php
php artisan snapshot:delete my-first-dump
```

##### To remove all backups except the most recent 2:
```php
php artisan snapshot:cleanup --keep=2
```
