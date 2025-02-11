### 📦 Runtrack Docker Jour 01

* Vérifier la version de Docker : 
```sh
docker --version
```

![alt text](images/docker-version.png)

* Tester les commandes de base : 

```sh
docker info
```

![alt text](images/docker-info.png)

```sh
docker ps
```

![alt text](images/docker-ps.png)

```sh
docker images
```

![alt text](images/docker-images.png)


```sh
docker run
```

![alt text](images/docker-run.png)


```sh
docker stop
```

![alt text](images/docker-stop.png)

* Récupérer l'image Docker

```sh
docker pull
```
Dans ce cas la on va pull l'image `nginx` pour la suite.

![alt text](images/docker-pull.png)


```sh
docker images
```

On utilise cette commande de nouveau avec cette fois ci un résultat différent.

![alt text](images/docker-images2.png)