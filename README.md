# docker-rails
Base files to be copied and modified in your rails app.

## Requirements
- Docker
- Docker Compose
- VirtualBox or native linux filesystem
- therubyracer gem for JS runtime environment

## Dockerfile
This is the basic docker setup, which composes of the essentials to have
a rails app running.

## docker-compose.yml
This builds up a cluster of docker instances to enable running a simple
rails application.

Inclusions are:
- Postgres (database)
- Redis (used for background process libraries such as sidekiq)
- Sidekiq
- Web (application)

## Usage
- Copy `database.yml.example` to your config directory
- Run `docker-compose build`
- Run `docker-compose run web bundle exec rake db:migrate`
- Run `docker-compose run web bundle exec rake db:seed` if you have a
  seeds file
- Run `docker-compose up`
- Get coding!
