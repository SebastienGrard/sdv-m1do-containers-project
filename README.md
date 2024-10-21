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

### API

#### Basics

Run `cargo build --release` to build and compile the app. This will create an executable in `/target/release/sdv-api`.

### Web

On the file named "sdv-m1do-containers-project/sdv-api/src/main.rs", you can add or remove Joke one the following section :

#[get("/")]
fn get_random_joke() -> Json<Joke> {
    let jokes = vec![
        Joke::new("CONTENT OF THE JOKE", "NAME_OF THE JOKE"),

     ];
    Json(jokes.choose(&mut rand::thread_rng()).unwrap().clone())
}

Add a line "Joke:new" with the right content to add a Joke to the Joke Of The Day.

#### Basics

Run `npm run build` to build the application, and run `npm run start` to start the Node.js server. 

#### Using Docker

Run 'docker-compose -f docker-compose.yml up --build -d' to build the application.




You can have access to the welcome portail on 'http://localhost:3000/', and the Joke Of The Day on 'http://localhost:3000/'
