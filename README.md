# rpi-docker-development

Lets make raspberry development easy by using docker:

1. Emulate an raspberry device on your development machine.

2. Develop your raspberry app by using docker container with full access to the hardware.

3. Build your rapsberry os image and deploy to sd card or simply pull the docker container on rspberry.

## Prepare your host

Install:
  * [docker](https://docs.docker.com/engine/installation/)
  * [docker-compose](https://docs.docker.com/compose/install/)


## Run raspberry on your host

Run in terminal `docker-compose up` and you will have a raspberry shell to work on.


## Setup docker and docker-compose on emulated raspberry

Run on raspberry emulation shell `/host/rpi/setup-docker`.

Or run on your development host `docker-compose run emulator /host/rpi/setup-docker`.

## Develop your raspberry docker app

You have to make sure to use a cross-buildable container base image or simply use the provided base image in `docker/rpi/base/Dockerfile` (look at `docker/rpi/docker-compose.yml` and `docker/rpi/wiringpi/Dockerfile`).

### Hello world
TODO

### Access gpio
TODO

### Deploy to your 'real world' raspberry
##### via sd card

##### via docker image update

## Limitations
### Sound

Sound is not supported as you have to pass your drive to the emulator instance. If you want to do so, uncomment the line `export QEMU_AUDIO_DRV=none` in file `docker/emulator/emulator-run` and rebuild the image ('docker-compose rebuild').

### GUI

At the moment there is no graphical user interface support. If you need one, a good point to start is to remove the `-nographic` parameter in `docker/emulator/emulator-run` and pass a device in `docker-compose.yml`.
