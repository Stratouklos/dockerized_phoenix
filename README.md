# Phoenix Dockerized Project Initializer

Heavily based on [Starting a Phoenix Project with Docker by Robert Beene](https://echobind.com/blog/using-phoenix-with-docker/)

## Usage

mkdir my_project
cd my_project
curl -L https://github.com/Stratouklos/phoenix_starter/releases/download/0.1/dockerized-phoenix.tar.gz | tar xvz
./init my_project

Subsequent init executions start the project and run ecto.create

## What it does

  * Creates a Phoenix image based on the official elixir:1.3.4
  * Starts a db container based on postgres:9.6-alpine
  * Configures config/dev.exs to talk to the db container
  * Starts a web container serving out of localhost:4000

## To release

git archive --format=tar.gz master > dockerized-phoenix.tar.gz
