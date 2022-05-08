<p align="center">
<a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a>
<a href="https://vuejs.org" target="_blank"><img src="https://gateway.pinata.cloud/ipfs/QmcpRC8XNi8Ko7NcdpJebWw3aiY2LKojja3btEiFnXnVk3" width="300"></a>
<a href="https://www.php.net"><br><img src="https://gateway.pinata.cloud/ipfs/QmfFReBkqLpRnEYz4zgSnU8YMHXQaPd5D8bfC8t6R1MuZj" width="200"></a>&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp
<a href=""><img src="https://gateway.pinata.cloud/ipfs/QmW4XaiTL6fCRHLMi1QzuiU8uGZYUKQsY28GTNqhKZSecK" width="120"></a>
</p>

# Laravel Installation Setps and Running:

<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="200"></a></p>

## Installation Via Composer :

```
> composer create-project laravel/laravel example-app

> cd example-app

> php artisan serve
```

## The Laravel Installer :

```
> composer global require laravel/installer

> laravel new example-app

> cd example-app

> php artisan serve
```

# Vuejs installation types in laravel :

<p align="center"><a href="https://vuejs.org" target="_blank"><img src="https://gateway.pinata.cloud/ipfs/QmcpRC8XNi8Ko7NcdpJebWw3aiY2LKojja3btEiFnXnVk3" width="200"></a></p>

## Vuejs official Installation Guide :

```
> npm init vue@latest
```

#### This command will install and execute create-vue, the official Vue project scaffolding tool. You will be presented with prompts for a number of optional features such as TypeScript and testing support:

```
✔ Project name: … <your-project-name>
✔ Add TypeScript? … No / Yes
✔ Add JSX Support? … No / Yes
✔ Add Vue Router for Single Page Application development? … No / Yes
✔ Add Pinia for state management? … No / Yes
✔ Add Vitest for Unit testing? … No / Yes
✔ Add Cypress for both Unit and End-to-End testing? … No / Yes
✔ Add ESLint for code quality? … No / Yes
✔ Add Prettier for code formatting? … No / Yes

Scaffolding project in ./<your-project-name>...
Done.
```

#### If you are unsure about an option, simply choose No by hitting enter for now. Once the project is created, follow the instructions to install dependencies and start the dev server:

```
> cd <your-project-name>
> npm install
> npm run dev
```

## composer install VueJs UI :

```
> composer require laravel/ui --dev
> php artisan ui vue --auth
```

## Vitejs VueJs official Installation Guide :

```
> npm create vite@latest my-vue-app -- --template vue
> cd my-vue-app
> npm install
> npm run dev
```

# Install the PHP MongoDB Driver

<p align="center"><a href="https://www.php.net"><img src="https://gateway.pinata.cloud/ipfs/QmfFReBkqLpRnEYz4zgSnU8YMHXQaPd5D8bfC8t6R1MuZj" width="150"></a></p>

## Install the PHP MongoDB Driver in Linux & Mac :

Before we can install the MongoDB libraries for Laravel, we need to install the PHP extension for MongoDB. Run the following command:

```
> sudo pecl install mongodb
```

You will also need to ensure that the mongodb extension is enabled in your php.ini file. The location of your php.ini file will vary depending on your operating system. Add the following line to your php.ini file:

```
extension="mongodb.so"
```

## Install the PHP MongoDB Driver in Windows :

### [MongoDB driver for PHP](https://pecl.php.net/package/mongodb)

### Paste the following php_mongodb.lib file in php/ext/ folder

### Paste the following code in php.ini file:

```
extension="mongodb"
```

# Installation MongoDB

<p align="center"><a href=""><img src="https://gateway.pinata.cloud/ipfs/QmW4XaiTL6fCRHLMi1QzuiU8uGZYUKQsY28GTNqhKZSecK" width="100"></a></p>

<p align="center"><a href="https://www.mongodb.com/try/download/community"><button>MongoDB Download</button></a></p>

# Install the laravel MongoDB package :

Lastly, run the following command from your Laravel project directory in order to add the MongoDB package for Laravel:

```
> composer require jenssegers/mongodb
```

config mongodb config config/app.php:

```php
 'providers' => [
    Jenssegers\Mongodb\MongodbServiceProvider::class,
],
```

# Configuring Your Laravel Project to Use MongoDB

## Configure MongoDB Database

Next, we need to set the database configuration in config/database.php. And putting this code:

```php
'default' => env('DB_CONNECTION', 'mongodb'),
```

And these codes as well:

```php
'mongodb' => [
    'driver'   => 'mongodb',
    'host'     => env('DB_HOST', 'localhost'),
    'port'     => env('DB_PORT', 27017),
    'database' => env('DB_DATABASE'),
    'username' => env('DB_USERNAME'),
    'password' => env('DB_PASSWORD'),
    'options'  => [
        'database' => 'admin' // sets the authentication database required by mongo 3
    ]
],
```

or this one, configuration, alternative:

```php
'mongodb' => [
    'driver'   => 'mongodb',
    'dsn' => env('DB_DSN'),
    'database' => env('DB_DATABASE'),
],
```

## Config the .env File

Open up .env file. use this config:

```
DB_CONNECTION=mongodb
DB_HOST=127.0.0.1
DB_PORT=27017
DB_DATABASE=database
DB_USERNAME=username
DB_PASSWORD=password
```

For alternative, use this config:

```
DB_CONNECTION=mongodb
DB_DSN=mongodb://username:password@127.0.0.1:27017/database_name
DB_DATABASE=database_name
```

## Replacing the eloquent:

Instead of using Illuminate eloquent by laravel, change and use the eloquent from jenssegers/mongodb:

```php
<?php
namespace App;
use Illuminate\Database\Eloquent\Model;
use Jenssegers\Mongodb\Eloquent\Model as Eloquent;
class ExampleController extends Eloquent {
    //
}
```

# environment variables of laravel :

-   config to connect to the mysql
-   config to connect to the postgresql
-   config to connect to the mongodb
-   config to connect to the redis server
-   config to connect to the filesystem
-   config to connect to the mailer
-   config to connect to the aws
-   config to connect to the app_url

.env file

```
APP_NAME=Laravel
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost

LOG_CHANNEL=stack
LOG_DEPRECATIONS_CHANNEL=null
LOG_LEVEL=debug

DB_CONNECTION=mongodb
DB_HOST=127.0.0.1
DB_PORT=27017
DB_DATABASE=database
DB_USERNAME=username
DB_PASSWORD=password

BROADCAST_DRIVER=log
CACHE_DRIVER=file
FILESYSTEM_DISK=local
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120

MEMCACHED_HOST=127.0.0.1

REDIS_HOST=127.0.0.1
REDIS_PASSWORD=null
REDIS_PORT=6379

MAIL_MAILER=smtp
MAIL_HOST=mailhog
MAIL_PORT=1025
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS="hello@example.com"
MAIL_FROM_NAME="${APP_NAME}"

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=
AWS_USE_PATH_STYLE_ENDPOINT=false

PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_APP_CLUSTER=mt1

MIX_PUSHER_APP_KEY="${PUSHER_APP_KEY}"
MIX_PUSHER_APP_CLUSTER="${PUSHER_APP_CLUSTER}"

```
