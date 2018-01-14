ARG runtime="nvidia"
FROM nvidia/cuda:8.0-runtime-ubuntu16.04

LABEL "maintainer"="Chris Diehl <cultclassik@gmail.com>"

# NVidia required env vars
ENV NVIDIA_VISIBLE_DEVICES=0
ENV NVIDIA_DRIVER_CAPABILITIES="compute,utility"

# Build env vars
ENV MINER_FILE="zm_0.5.8.tar.gz"
ENV MINER_URL="https://s3-us-west-1.amazonaws.com/mastermine/minebox/${MINER_FILE}"

RUN apt-get update && apt-get install -y --no-install-recommends \
    wget \
 && rm -rf /var/lib/apt/lists/* \
 && mkdir /miner \
 && wget --no-check-certificate $MINER_URL \
 && tar -xvf $MINER_FILE -C /miner --strip-components 1 \
 && rm $MINER_FILE

WORKDIR /miner

# API port
EXPOSE 2222/tcp

ENTRYPOINT [ "/miner/zm" ]
CMD [ "--server", "hostname", "--port", "port", "--user", "user", "--pass", "pass", "--telemetry", "0.0.0.0:2222" ]
