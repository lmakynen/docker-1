# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lmakynen <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/08/14 17:30:10 by lmakynen          #+#    #+#              #
#    Updated: 2020/08/15 17:13:21 by lmakynen         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian

MAINTAINER lmakynen <lmakynen@student.hive.fi>

ENV TS3SERVER_LICENSE=accept

EXPOSE 9987/udp 10011 30033

WORKDIR /home/teamspeak

RUN apt-get update && apt-get upgrade -y && \
	apt-get install -y wget bzip2 && \
	wget http://dl.4players.de/ts/releases/3.12.1/teamspeak3-server_linux_amd64-3.12.1.tar.bz2 && \
	tar xvf teamspeak3-server_linux_amd64-3.12.1.tar.bz2
	
WORKDIR teamspeak3-server_linux_amd64

ENTRYPOINT sh ts3server_minimal_runscript.sh

# To build: docker build -t ex01 .
# To run: docker run -it --rm -p 9987:9987/udp -p 10011:10011 -p 30033:30033 ex01
# To get the ip and keytoken: docker-machine ip Char
#
# With this one person can join the server (which is enough according to the subject).
# If you want more people to join, you have to set up VM
# Stop the VM Char: docker-machine stop Char
# Go to the VM settings/network/adapter3/enable network adapter/bridge adapter/en0:Ethernet/
# advanced/adapter type /intel pro/1000 MT Desktop/ ok
# Start the machine again: docker-machine start Char and activeted it!
# run this command: docker-machine regenerate-certs Char
# connect via ssh to your VM: docker-machine ssh Char
# ifconfig -a / copy the inet add: 10.13.x.x from eth2.
# exit ssh connection
# Build and Run the Ts3 server
# Connect in the Client with the eth2 IP and the Token you received
# A user can join now your server.
