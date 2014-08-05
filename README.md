# Flock

## Overview
Flock, the super-simple social-stream for your business.

**Note** This project is still at its earliest stages.

## Server
The backend API is written in PHP and uses the Laravel framework.

Change into the server directory, install all composer packages and run the API server with Artisan.

**Note** *This assumes that you've aliased 'php artisan' and 'php composer'. If not, alias the commands or prepend the commands in question with 'php'.*
	
	cd server
	composer install
	artisan serve
	
## Client
The client, single page application is written in AngularJS. The client also makes use of Twitter Bootstrap etc. The asset pipeline is handled by Gulp, so please make sure you've node.js installed. Change into the client directory and install all node & Bower modules before attempting to use Gulp.

	cd client
	npm install && bower install
	gulp serve

	
#### Gulp Tasks
* `gulp` or `gulp build` to build an optimized version of your application in */server/public*. The index file is placed in */server/app/views/* as *index.blade.html*
* `gulp serve` to launch a browser sync server on your source files
* `gulp serve:dist` to launch a server on your optimized application
* `gulp wiredep` to fill bower dependencies in your .html file(s)
* `gulp test` to launch your unit tests with Karma
* `gulp protractor` to launch your e2e tests with Protractor
* `gulp protractor:dist` to launch your e2e tests with Protractor on the dist files
