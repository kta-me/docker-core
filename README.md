#  Docker Compose

An environment built using Docker Compose. It consists of the following:

* PHP
* Apache
* Nginx
* MySQL
* phpMyAdmin
* Redis

You can chose one of several different PHP versions:

* 7.2.x
* 7.4.x
 
##  Installation
 
* clone this repository on your local computer
* configure .env as needed in folder www/test
* Run the `docker-compose up -d`.

```shell
git clone https://github.com/katvat/docker-core.git
cd docker-core/www/test
// modify .env as needed
docker-compose up -d
// visit in browser http://localhost/
```
You can access via http://localhost/

## phpMyAdmin

phpMyAdmin is configured to run on port 8081. Use following default credentials.

http://localhost:8081/  

username: test  or  root

password: 111

### General Information 
It will be started `index.php` from folder `www/test/src/public`.
If you would like to run project from folder `www/test/src` just edit `.htaccess` file in folder `www/test/src`.

## Redis

It runs on default port `6379`.

Enjoy! 
