> This repository stores notes on using the CLI docker-compose.

Docker Compose is a tool for defining and running multi-container Docker applications.
With Compose, you use a YAML file (`docker-compose.yml`) to configure your application’s services,
networks, and volumes. Then, with a single command, you create and start all the services.

## Install

Of course, please install docker first!
You may find a handy installation script in this [link](https://github.com/bruceChanJianLe/ansible-docker).

For Ubuntu:  
```bash
sudo apt-get install docker-compose-plugin
```

For Arch:  
```bash
sudo pacman -S docker-compse
```

## Usage

Command                        | Description                                                                 
---|---
`docker-compose up`           | Builds, (re)creates, starts, and attaches to containers for a service.
`docker-compose up -d`        | Starts containers in detached mode (in the background).
`docker-compose down`         | Stops and removes containers, networks, volumes, and images created by `up`.
`docker-compose build`        | Builds or rebuilds services defined in the `docker-compose.yml`.
`docker-compose stop`         | Stops running containers without removing them.
`docker-compose start`        | Starts existing stopped containers.
`docker-compose ps`           | Lists containers managed by Docker Compose.
`docker-compose logs`         | Views output from containers.
`docker-compose exec [svc] bash` | Opens a Bash shell inside a running container (e.g., service = `web`).
`docker-compose config`       | Validates and displays the final Compose configuration.


## Notes

`docker-compose up` == `docker-compose build && docker-compose create && docker-compose run`
