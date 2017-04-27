FROM armhf/debian:jessie

RUN apt-get update && \
	apt-get install -y --no-install-recommends apt-transport-https wget ca-certificates && \
	wget https://homegear.eu/packages/Release.key && apt-key add Release.key && rm Release.key && \
	echo 'deb https://homegear.eu/packages/Debian/ jessie/' > /etc/apt/sources.list.d/homegear.list && \
	apt-get update && \
	apt-get install homegear homegear-homematicbidcos homegear-homematicwired && \
	apt-get clean && rm -rf /var/lib/apt/lists/*
