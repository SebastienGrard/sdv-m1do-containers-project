# Sup de Vinci - Containers module project

*Tested with `rust v1.82.0` et `node 23.0.0`.*

LIEN VERS LE DOCKERHUB

https://hub.docker.com/repositories/sebastiengrard


## Development

### API

#### Basics

Use `cargo run` to start the dev environment.

You can also install [cargo-watch](https://crates.io/crates/cargo-watch) to watche over your project's source for changes, and runs Cargo commands when they occur : `cargo-watch -x run`.

#### Using Docker

 Use 'docker build -t sdv-api .' to build the Docker, and 'docker run sdv-api' to start the dev environment.           

### Web

#### Basics

Use `npm install` to install all dependancies, and `npm run dev` to start the dev environment.

#### Using Docker

 Use 'docker build -t sdv-web .' to build the Docker, and 'docker run sdv-web' to start the dev environment.

## Production

You need to get Docker and Git on your distribution.
You can use Docker Desktop and VSCode on Windows, for example

You can clone this repo on your environment, in order to use it.
Go in the parent folder of the repo in order to make it work.

Execute the following command 'docker-compose --build' to start the building of the environment.

Open 'localhost:3000' in a browser to connect with the Front End.
Open localhost:80 in an internet browser to connect with the API.

You can also use the command 'curl' to get the content of the website page.

If you want to use the Docker image, you can find it on the Docker Hub. The link is : 'https://hub.docker.com/repositories/sebastiengrard'