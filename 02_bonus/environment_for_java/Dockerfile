# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lmakynen <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/08/19 20:26:21 by lmakynen          #+#    #+#              #
#    Updated: 2020/08/19 20:28:33 by lmakynen         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu

MAINTAINER lmakynen <lmakynen@student.hive.fi>

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y default-jdk && apt-get install -y default-jre git vim emacs

# To build: docker build -t java .
# To run: docker run -ti --rm java
