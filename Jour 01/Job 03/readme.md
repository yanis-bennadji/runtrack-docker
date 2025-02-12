### 📦 Runtrack Docker Day 01 Job 03

* The goal in this Job is to learn how to learn more deeply the usage of Docker Desktop and how to use different images we can find online.


#### 🔎 Search an image with Docker Desktop

The first step is to open Docker Desktop, go insinde the "images" menu on the left side bar and access the terminal located at the bottom right of bottom Desktop.

![alt text](images/docker-desktop1.png)

Now that we have opened the terminal we are gonna look for an image called `pengbai/supermario` using the following command : 

```sh
docker search pengbai/supermario
```

![alt text](images/docker-desktopSearch.png)

Let's pull it so we can have it on our computer : 

```sh
docker pull pengbai/docker-supermario
```

You will notice after this that it appears on your Images list in Docker Desktop now.

