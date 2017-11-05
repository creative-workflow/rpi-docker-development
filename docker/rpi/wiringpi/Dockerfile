FROM rpi_base:latest

RUN apk update && apk upgrade

RUN apk add htop curl bash

# kotlin
# RUN apk add zip unzip
# RUN curl -s "https://get.sdkman.io" | bash
# RUN source "$HOME/.sdkman/bin/sdkman-init.sh"
# RUN sdk install java kotlin

# wiringpi
RUN apk add make raspberrypi raspberrypi-dev g++ git
RUN git clone https://github.com/WiringPi/WiringPi.git && \
    cd WiringPi/wiringPi && \
    make static

RUN curl https://pi-control.de/pic_installer | bash
