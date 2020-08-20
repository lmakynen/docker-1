# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lmakynen <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/08/20 15:35:36 by lmakynen          #+#    #+#              #
#    Updated: 2020/08/20 15:54:09 by lmakynen         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu

MAINTAINER lmakynen <lmakynen@student.hive.fi>

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y cowsay

# Prepares a command that runs cowsay when the image is executed.
CMD ["/usr/games/cowsay", "MooOOoO, YOU CAN DO THIS!<3"]

# To build: docker build -t cowsay .
# To run: docker run --rm cowsay
