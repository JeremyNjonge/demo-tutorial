# demo-tutorial

We are going to create a laravel , vue3 and inertiaJS project

Requires composer, php, node and npm already installed

Install Laravel by running the command composer create-project --prefer-dist laravel/laravel projectname in your terminal. This will create a new Laravel project in a directory called "projectname".

Install the Breeze package by running the command composer require laravel/breeze --dev

Run the command php artisan breeze:install to install the Breeze scaffolding.

Install the InertiaJS package by running the command composer require inertiajs/inertia-laravel

Go to the resources/js folder and delete the app.js file and create a new file main.js


In the main.js file, you can include the following code:

import { createApp } from 'vue'
import { InertiaApp } from 'inertia-vue'

const app = createApp(InertiaApp)

app.mount('#app')



In webpack.mix.js

mix.js('resources/js/main.js', 'public/js')
    .sass('resources/sass/app.scss', 'public/css');


In app/Providers/AppServiceProvider.php

use Inertia\Inertia;

class AppServiceProvider extends ServiceProvider
{
    public function boot()
    {
        Inertia::setRootView('app');
    }
}


Run npm install && npm run dev to install the necessary dependencies and build the front-end assets.

Start the development server by running the command php artisan serve and you should be able to access your new project in your browser at http://localhost:8000.

For official documentation

https://laravel.com/docs/9.x/breeze
