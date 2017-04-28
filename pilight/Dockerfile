FROM armhf/debian:jessie

RUN apt-get update && \
	apt-get install -y --no-install-recommends apt-transport-https wget ca-certificates && \
	wget -O - https://apt.pilight.org/pilight.key | apt-key add - && \
	echo 'deb https://apt.pilight.org/ stable main' > /etc/apt/sources.list.d/pilight.list && \
	apt-get update && \
	apt-get install -y --no-install-recommends pilight && \
	apt-get clean && rm -rf /var/lib/apt/lists/*
