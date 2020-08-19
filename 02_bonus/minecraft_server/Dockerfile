# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lmakynen <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/08/19 19:47:06 by lmakynen          #+#    #+#              #
#    Updated: 2020/08/19 20:04:42 by lmakynen         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu:18.04

MAINTAINER lmakynen <lmakynen@student.hive.fi>

# Updating and installing the necessary dependencies (Java and Wget).

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y wget default-jdk
RUN mkdir minecraft

WORKDIR minecraft

RUN wget https://launcher.mojang.com/v1/objects/c5f6fb23c3876461d46ec380421e42b289789530/server.jar

# You need to agree to the EULA in order to run the server.

RUN echo "eula=true" > eula.txt

EXPOSE 25565

# The flag Xmx specifies the maximum memory allocation pool for a Java virtual machine, while Xms specifies the initial memory allocation pool. nogui starts the server without a GUI (GUI is graphical user interface). 

ENTRYPOINT java -Xmx1024M -Xms1024M -jar server.jar nogui

# To build: docker build -t mc-server .
# To run: docker run -ti --rm -p 25565:25565 mc-server
