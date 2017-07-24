# simple-student-information-system
A dead simple system that I did when I was learning basic PHP and AWS RDS.


STPES to Install :

1. create ubuntu 16 ec2 
2. Create AWS mysql RDS 



Requirement :
php, php-mysql, mysql clint, apache2

Set up your Ubuntu EC2 instance with LAMP stack – Linux, Apache, MySQL, PHP. I have used Ubuntu 16.04 machine. To know how to set up an instance in AWS, check this post.

Step 1: Installing Apache 2.4

$ sudo apt-get install apache2

Step 2: Installing MySQL
You will be prompted for username and password for database.

$ sudo apt-get install mysql-server

Step 3: Installing PHP
You need to include some helper packages for mod, mysql and mcrypt.

$ sudo apt-get install php libapache2-mod-php php-mcrypt php-mysql

Step 4: Modify permission (optional)
By default, /var/www/html directory will not be available to write unless you are a super user. So grant full permission for html directory.

$ sudo chmod 777 /var/www/html/

Step 5: Test installation

Create a file (say index.php) in /var/www/html/ and paste the following:

<?php
phpinfo();

Now, open your instance endpoint in your browser and access the file you created. In my case,

http://<my-ip>/index.php

If you see PHP information page, you are all set!
