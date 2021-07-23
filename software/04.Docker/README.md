# Workshop 4 - Docker for beginners

✔️ Learn docker CLI

✔️ Use docker container

✔️ Create your own image

✔️ Manage many containers through docker-compose

## Step 0: Initialization

All the required information to install dependencies can be found in [SETUP.md](./SETUP.md).

## Story

You are a software engineer in a high potential startup.

Your first version is ready to be deployed, however your manager wants the deployment to be simple, fast and does not require a manual configuration of the server on which you will deploy.

For this, you quickly search on google and come across a great containerization tool called Docker.

Docker is a tool capable of encapsulating an application in a container which allows you to run it in an isolated and controlled environment. This makes deployment much easier since you only need to have Docker installed on your machine and you're done.
No more need for a big script to manage dependencies, no more need to adapt to the machine, the container is isolated and is self sufficient.

## Step 1: The bases of Docker

Having no knowledge of docker, you first decide to take over the CLI based on your experience at Epitech.
Let's learn how to use the "moulinette"'s docker to test your EPITECH projects.
- Download and run the ["moulinette"](https://hub.docker.com/r/epitechcontent/epitest-docker/) 's image.
- Using `docker run` command and some arguments:
  - mount your current directory `$PWD` in your container
  - launch a shell to execute commands in your container
  - execute `cat /etc/os-release | grep PRETTY_NAME` , you should get `Fedora 32 (Container Image)`
- Now, find the command to display images, containers, volumes and networks.

> [There is a document in the intranet that can help you](https://intra.epitech.eu/file/public/technical-documentations/doc_docker.pdf) (but be careful when copying the commands, there are many extra spaces due to PDF formatting)

## Step 2: Containerization of an API with a Dockerfile

Now, we will learn how to build a custom docker image thanks to a `Dockerfile`.

In the [src](./src/node_api) folder, you'll find a NodeJS API. This API is very simple, it returns a message when you do a GET request on `/`.
In a first time, download the API [here](https://downgit.github.io/#/home?url=https://github.com/PoCInnovation/Workshops/tree/master/software/04.Docker/src/node_api).

The objective is to create a docker image of that API. You must:

- Create a `Dockerfile` in the `node_api` folder.

- Build an `image` from `node:12-alpine`.
- Copy the code from the API in the image.
- Define the environment variable `PORT` that indicate on which port the API must listen.
- Make the API accessible from outside the image on the same port as `PORT`.
- Install dependencies (`npm install`) and launch the API (`npm start`).

> Take a look at the [documentation](https://docs.docker.com/engine/reference/builder/) about Dockerfiles.

Once your image is created, you must `run` a container based on it.

> You will need to use the commands `docker build` and `docker run` (with some extra arguments of course)<br>
> Curl can be useful to test your API on `http://localhost:8080` , or simply open the URL in your browser

You now have a docker image which contains a node API and everything necessary to run it, with only Docker installed on your computer. Say farewell to installations that destroy your dump!

## Step 3: Containerization of Epytodo with a docker-compose

To finish, you will containerize your `Epytodo` project. If you do not have one, we give you a downloadable tar file in the [src](./src/epytodo) directory, **but use yours if it works!**

 To do that, you will create:
- A `Dockerfile` to build the image of your API (like in Step 2, but the API is in python, so dependencies installation will be different). You must use the `python:3.7.5-alpine` image
- A `docker-compose.yml` to create and link the database to your API

Your folder structure should look like this:

```
├── docker-compose.yml
└── epytodo
    └── Dockerfile
```

Your docker-compose will have 2 services:
- `app`: Launchs your Flask API (created by your Dockerfile)
- `db`: Launchs your `mariadb` database (more information [here](https://hub.docker.com/_/mariadb))

Here is a base to start off your `docker-compose.yml`

<Details><Summary><strong>docker-compose.yml</strong></Summary>

```yaml
version: "3"

services:
  app:
    container_name: api

  db:
    container_name: database

volumes:
  mysql-data:

networks:
  epytodo-network:
```

</Details>

We want `app` and `db` to be able to communicate properly, so we are going to put them on the same network, `epytodo-network`. Moreover, if we want to keep our database data even when the container is stopped, we have to save it's data in a volume, `mysql-data`.

`app` properties:

- `build`: defines the image you'll build before running the service
- `ports`: ports redirection between host and container
- `environment`: environment variables required to run the image (check the database credentials used to connect to mysql in `config.py`)
- `networks`: to be able to reach the database
- `restart`: to specify what to do if the container stops

`db` properties:

- `image`: defines which image you'll base the service on
- `ports`: ports redirection between host and container
- `environment`: environment variables required to run the image (find them [here](https://hub.docker.com/_/mariadb))
- `networks`: to allow the app to reach the database
- `volumes`: to specify which volume you'll use to save the data, and to load `epytodo.sql` on database initialization

:warning: The database inside the `db` container must be named `epytodo`, as written in the sql file.

> Documentation on how [docker-compose](https://docs.docker.com/compose/) works.<br>
> What is the default port of your flask/mysql services ?<br>
> Don't forget to use `alpine` images rather than default images, and avoid `latest` versions in general

If you did this step correctly, your Epytodo should be accessible as if it were manually launched with python.

Congratulation, you are now ready to create a docker image of your product !

## To go further

If you want to learn more on the architecture implementation and container's management, you can check those links:
- [Kubernetes](https://kubernetes.io/fr/docs/concepts/overview/what-is-kubernetes/)
- [Lazydocker](https://github.com/jesseduffield/lazydocker)
- [Docker hub](https://hub.docker.com/)
- [Docker swarm](https://docs.docker.com/get-started/swarm-deploy/)

## Authors
- [Tom Chauveau](https://github.com/TomChv)
- [Jérome Collet](https://github.com/JeromeCGithub)
- [Paul Monnery](https://github.com/PaulMonnery/)

## Organization

- [📒 Linkedin](https://www.linkedin.com/company/pocinnovation/mycompany/)
- [📷 Instagram](https://www.instagram.com/pocinnovation/)
- [🖱️ Website](https://www.poc-innovation.fr/)
- [🌐 Discord](https://discord.gg/Yqq2ADGDS7)

> :rocket: Don't hesitate to follow us on our different networks, and put a star 🌟 on `PoC's` repositories.
