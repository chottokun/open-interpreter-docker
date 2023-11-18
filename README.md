# open-interpreter-docker

[Open Interpreter](https://github.com/KillianLucas/open-interpreter) docker environment

## Setup

Execute following command:

```sh
$ cd && git clone https://github.com/karaage0703/open-interpreter-docker
```

## Simple

### Docker build

```sh
$ cd ~/open-interpreter-docker
$ docker build -t open-interpreter-simple ./container-simple
```

### Docker run

```sh
$ cd ~/open-interpreter-docker
$ docker run -it --rm -v $(pwd):/root open-interpreter-simple

# with environmental variables
$ docker run -it --rm -e OPENAI_API_KEY=<OPENAI_API_KEY> -v $(pwd):/root open-interpreter-simple
```

## Local

### Docker build

```sh
$ cd ~/open-interpreter-local
$ docker build -t open-interpreter-local ./container-local
```

### Docker run
1. Run [LM Studio](https://lmstudio.ai/) and turn on server mode.
1. 

```sh
docker run --rm -it --add-host=localhost:xx.xx.xx.xx open-interpreter-local bash
```
xx.xx.xx.xx : LM Studio server ip address.

### Run app
Execute following command in container:

```sh
root@hostname:~# interpreter -y --local
```

And enjoy open interpreter with local LLM.


## GUI

### Docker build

```sh
$ cd ~/open-interpreter-docker
$ docker build -t open-interpreter-gui ./container-gui
```

### Docker run

```sh
$ cd ~/open-interpreter-docker
$ docker run --rm -v $(pwd):/root -p 6080:80 open-interpreter-gui

# with environmental variables
$ docker run --rm -e OPENAI_API_KEY=<OPENAI_API_KEY> -v $(pwd):/root -p 6080:80 open-interpreter-gui
```

### Run app

Browse http://127.0.0.1:6080/

Enjoy open interpreter


## References
- https://note.com/masia02/n/n630d091c4a02
- https://github.com/Frederic-Boulanger-UPS/docker-ubuntu_22-04-novnc
- https://rooter.jp/infra-ops/build_docker_jp_env/
