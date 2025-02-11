### 📦 Runtrack Docker Day 01 Job 02

* The goal here is to learn how to work with Docker using this repository :
  
https://github.com/docker/welcome-to-docker

Lets see now step by step how we are gonna do this.

* Start by cloning the repository
  
* Now you should be able to see the repository in VSCode like this :
  
  ![alt text](images/vscode-screen1.png)

  Take a look at the different files you have and you should find the `Dockerfile`. The next step is using this file to create an image that we will use with Docker.

  #### 🛠️ Lets build an image with a Dockerfile

* The first step is to open the VSCode terminal in our repository to make sur we are inside the right folder, our terminal should look like this : 

![alt text](images/vscode-terminal1.png)

* Now lets build the image in the terminal with this command line :

```sh
docker build -t <name_of_the_image> .
```

In this command the `-t` flag is used to give a name to the image and the `.` at the end specifies the `build` context as the current directory to look for the Dockerfile. In this case I decided to call this image `welcome-to-docker`.

After using this command line you should see this : 

![alt text](images/vscode-terminal-finished.png)

(It can take a bit of time to build, in my case it took 94.1s) and if we take a look at our Docker Desktop we can see that image is here :

![alt text](images/docker-screen1.png)


* Lets run the image to make sure everything is right let's run this image by creating a container from it

We are gonna use this command line to create the container :

```sh
docker run -d -p 8088:3000 --name welcome-to-docker welcome-to-docker
```
And then use the next command to check if the container is running

```sh
docker ps
```

![alt text](images/vscode-terminal-container.png)


* Now let's check if we can check the container on our browser ! 

We are gonna go to this adress `localhost:8088` and if you followed the steps before correctly you should see this : 

![alt text](images/chrome-container.png)

Perfect ! Now lets see if we can change a bit this page so it feels a bit more personal.

