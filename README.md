# base-angular4-environment

> Dockerized Angular 4 Application

## Requirements

* [Docker Engine](https://docs.docker.com/installation/)
* [Docker Compose](https://docs.docker.com/compose/)

# Running Locally

## Setup
- Linux (or a VM)
- Get [docker](https://docker.com)
- Get [docker-compose](https://github.com/docker/compose)
- Run the following comand (only after installing docker)

  ```
  docker run -d -t --restart=always -p 80:80 -v /var/run/docker.sock:/tmp/docker.sock:ro --name=nginx-domain-proxy jwilder/nginx-proxy
  ```

  ```
  docker network create -d bridge nginx-domain-proxy
  ```

  ```
  docker network connect nginx-domain-proxy nginx-domain-proxy
  ```

- reboot

# Running

```sh
$ docker-compose up
```

## License

Copyright &copy; 2017 [Daniel Dias Branco Arthaud](http://github.com/darthaud). Licensed under the terms of the [MIT license](LICENSE.md).
