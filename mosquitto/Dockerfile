FROM armhf/debian:jessie

RUN apt-get update && \
	apt-get install -y --no-install-recommends apt-transport-https wget ca-certificates && \
	wget http://repo.mosquitto.org/debian/mosquitto-repo.gpg.key && apt-key add mosquitto-repo.gpg.key && rm mosquitto-repo.gpg.key && \
	echo 'deb http://repo.mosquitto.org/debian jessie main' > /etc/apt/sources.list.d/mosquitto.list && \
	apt-get update && \
	apt-get install -y --no-install-recommends mosquitto && \
	apt-get clean && rm -rf /var/lib/apt/lists/*
