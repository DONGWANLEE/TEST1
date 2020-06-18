## Refactoring 과제

이 프로젝트는 [bestmomo/laravel5-5-example](https://github.com/bestmomo/laravel5-5-example)을 기초로 합니다.
DB는 편의상 sqlite에서 동작하도록 설정합니다.
아래 [Installation](#installation)을 따라 초기화 하신 후, `php artisan serve`로 샘플 페이지를 구동하실 수 있습니다.

## Laravel 5-5 example ##

**Laravel 5-5 example** is a tutorial application.

### Installation ###

* type `git clone https://github.com/bestmomo/laravel5-5-example.git projectname` to clone the repository 
* type `cd projectname`
* type `composer install`
* copy *.env.example* to *.env*
* type `php artisan key:generate`to generate secure key in *.env* file
* type `touch database/database.sqlite` to create the file
* type `php artisan vendor:publish --provider="Bestmomo\LaravelEmailConfirmation\ServiceProvider" --tag="confirmation:migrations"` to publish email confirmation migration
* type `php artisan migrate --seed` to create and populate tables
* edit *.env* for emails configuration

### Include ###

* [Styleshout](https://www.styleshout.com/) for front template
* [CKEditor](http://ckeditor.com) the great editor
* [Elfinder](https://github.com/Studio-42/elFinder) the nice file manager
* [Sweet Alert](http://t4t5.github.io/sweetalert/) for the cool alerts
* [AdminLTE](https://adminlte.io/themes/AdminLTE/index2.html) the great admin template
* [Gravatar](https://github.com/creativeorange/gravatar) the Gravatar package
* [Intervention Image](http://image.intervention.io/) for image manipulation
* [Email confirmation](https://github.com/bestmomo/laravel-email-confirmation) the package for email confirmation
* [Artisan language](https://github.com/bestmomo/laravel-artisan-language) the package for language strings management
* [Laravel debugbar](https://github.com/barryvdh/laravel-debugbar)
* [Etrepat baum](https://github.com/etrepat/baum) for comments management

### Features ###

* Home page
* Custom error pages 403, 404 and 503
* Authentication (registration, login, logout, password reset, mail confirmation, throttle)
* Users roles : administrator (all access), redactor (create and edit post, upload and use medias in personnal directory), and user (create comment in blog)
* Blog with nested comments
* Search in posts
* Tags on posts
* Contact us page
* Admin dashboard with users, posts, articles, medias, settings, notifications and comments
* Multi users medias gestion
* Localization (English, French and Chinese)
* Application tests
* Thumbs creation for images
* Notifications to send emails and notify redactors for new comments

### Tricks ###

To use application the database is seeding with users :

* Administrator : email = admin@la.fr, password = admin
* Redactor : email = redac@la.fr, password = redac
* User : email = walker@la.fr, password = walker
* User : email = slacker@la.fr, password = slacker

### Tests ###

When you want to launch the tests refresh and populate the database :

`php artisan migrate:fresh --seed`

You must have default settings and **en** language. You must also add provider in **config/app.php**.

You can then use Dusk.

### License ###

This example for Laravel is open-sourced software licensed under the MIT license
