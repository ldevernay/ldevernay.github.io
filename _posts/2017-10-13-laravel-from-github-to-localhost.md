---
layout: post
title:  "Laravel - from github to localhost"
date:   2017-10-13 12:00:00 +0200
categories: code
---

Some useful (and badly documented) tricks to use an existing Laravel project locally without getting ugly cryptic errors.   
> Spoiler alert : this might prove useful when deploying to another server.   
  
When using Laravel, you will often find yourself fetching a new project from Github to deploy it locally (e.g. when working in a team).  
Unfortunately such an operation needs you to run some hard-to-find commands. Once again, I wandered a lot before finding these. Laravel is powerful and mostly-well-documented but all this nice magic comes with a cost.  

## Initiate the database
Change the database configuration in .env and app/config/database.php (assuming you want to use a local database which you already have created).  
Open your terminal and run these commands :  

```
composer install
(all dependencies are installed)
php artisan migrate
(create data tables)
php artisan db:seed
(run the seeds)
```
  
## The trouble with ciphers
Suddenly, one of theses famous cryptic errors :

```
The only supported ciphers are AES-128-CBC and AES-256-CBC
```
  
Sure, why not…  
Good news is you only have to run two commands to get rid of that :

```
php artisan key:generate
php artisan config:clear
```
  
After that, you can finally run your server locally.  

```
php artisan serve
```

Enjoy!