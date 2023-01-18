# demo-tutorial

We are going to create a laravel , vue3 and inertiaJS project

Requires composer, php, node and npm already installed

Install Laravel by running the command composer create-project --prefer-dist laravel/laravel "projectname" in your terminal. This will create a new Laravel project in a directory called "projectname".

Install the Vue 3.0 package by running the command composer require laravel/jetstream in your terminal.

Install InertiaJS package by running the command composer require inertiajs/inertia-laravel

Run the command php artisan jetstream:install inertia to install Jetstream with InertiaJS.

Run npm install && npm run dev to install the necessary dependencies and build the front-end assets.

Finally, start the development server by running the command php artisan serve and you should be able to access your new project in your browser at http://localhost:8000.