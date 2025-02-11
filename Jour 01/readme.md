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

* Construisez le container Docker 

On va utiliser la commande suivante :

```sh
docker run -it --rm -p --name first-container 8080:80 nginx
```

Cela nous permet de créer un container temporaire nginx.

![alt text](images/docker-run2.png)

Sur Docker Desktop on vois également le résultat.

![alt text](images/docker-desktop.png)

* Arrêter votre container 

Comme notre container est en mode interactif avec `-it`, on stop le container avec `CTRL+C` et il se supprimera automatiquement avec `--rm`.

Dans le cas ou notre container est en mode détaché avec `-d`, il faudra écrire dans un autre terminal la commande suivante : 

```sh
docker stop first-container
```

![alt text](images/docker-stop2.png)


* Supprimer votre container

Dans le cas ou notre commande ne contient pas `--rm` on dois utiliser la commmande suivante : 

```sh
docker rm first-container
```

![alt text](images/docker-rm.png)

Il faut bien penser à stop le container avant de le supprimer, sinon il est possible de forcer l'arrêt et la suppression en une seule commande : 

```sh
docker rm -f first-container
```

* Supprimer vot