# Docker-DevOps

Docker-DevOps is a stack of containers providing a complete web development environment like XAMPP.

It contains from default:
1. a MySQL container to provide database
2. a PHPMyAdmin container to manage database and tables
3. a PHP as FPM container to provide php with own php.ini
4. an Apache webserver
5. a FTP service to manage files if you want like a real webserver

NOTE:
This should only be for local development! All ports are open like XAMPP and everyone in the local network have access!

Usage:
1. edit the .env file and set:
   in line 1-3 wanted versions of PHP, MySQL and Apache server
   in line 5 the database root password
   in line 7-8 the FTP credentials
2. edit the html/index.php and set your database password
3. optional edit the php/php.ini if required
4. optional edit the phpmyadmin/config.user.inc.php if required
5. optional edit the docker-compose.yml if you want
   other ports
   additional volumes
   extra hosts see on line #47
   other user-uid-gid on line #125
   other networks on line #128
