FROM debian:jessie

RUN apt-get update && apt-get install -y qemu-system-arm git wget unzip file

COPY ./emulator-prepare /emulator-prepare
RUN chmod +x /emulator-prepare

COPY ./emulator-run /emulator-run
RUN chmod +x /emulator-run

VOLUME ["/emulator-data", "/host"]

ENTRYPOINT ["/emulator-prepare && /emulator-run"]
