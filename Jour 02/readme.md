### 📦 Runtrack Docker Day 02 Job 01

* The goal in this Job is to learn how to include an apache server into a Docker image.


#### 🌐 Preparing everything

The first thing we are gonna do is create an `index.php` that will show the different informations about the server and a `Dockerfile` that will create an apache environment.

In `index.php`, you will just put :

```php
<?php 

phpinfo();

?>
```

It will allow us to show the informations about the apache server later.
Now for the `Dockerfile` we will put : 

```docker
FROM php:8-apache

WORKDIR /var/www/html

RUN echo "<?php phpinfo(); ?>" > index.php

EXPOSE 80

```

It will create an apache server and show us the `index.php`


#### 🌐 Using Docker now

Now it's time to create create our image from our `Dockerfile` and run a container with it.

```sh
docker build -t apache-image .
```

```sh
docker run -d -name apache-container -p 8080:80 apache-image
```

Now if we go to `localhost:8080`, we should be able to see all the informations about our server running like this : 

![alt text](<Job 01/images/phpinfo.png>)

You can now see all the informations you want, you can now stop the container using : 

```sh
docker stop apache-container
```