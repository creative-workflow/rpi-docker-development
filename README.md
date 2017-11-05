# rpi-docker-development

Lets make raspberry development easy by using docker to emulate an raspberry on your host machine.

Second use docker to develop services for the raspberry with full access to the hardware.

# Prepare your host

Install:
  * [docker](https://docs.docker.com/engine/installation/)
  * [docker-compose](https://docs.docker.com/compose/install/)


# Run raspberry on your host

Just run 'docker-compose up' and you will get an raspberry terminal.


# Setup docker and docker-compose on raspberry

Run `docker-compose run emulator /host/rpi/setup-docker` on your host mashine.

# Develop container for raspberry

You have to make shure to use

### Hello world
### Access gpio
### Deploy to you real world raspberry


# Limitations
### Sound

Sound is not supported as you have to specifi your drive to the emulator image. If you want to do so uncomment the line `export QEMU_AUDIO_DRV=none` in the `docker/emulator/prepare-emulator` file and re build the image.
