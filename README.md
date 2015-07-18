# docker-rails
Base files to be copied and modified in your rails app.

## Requirements
- Docker
- Docker Compose
- VirtualBox or native linux filesystem

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
