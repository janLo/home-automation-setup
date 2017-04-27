FROM armhf/debian:jessie

RUN apt-get update && apt-get upgrade && \
	apt-get install i--no-install-recommends \
		build-essential \
		libusb-1.0-0-dev \
	apt-get clean && rm -rf /var/lib/apt/lists/*

ADD hmcfgusb /hmcfgusb
WORKDIR /hmcfgusb
RUN cd /hmcfgusb && make
