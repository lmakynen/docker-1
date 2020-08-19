# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lmakynen <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/08/19 20:16:01 by lmakynen          #+#    #+#              #
#    Updated: 2020/08/19 20:18:07 by lmakynen         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian

MAINTAINER lmakynen <lmakynen@student.hive.fi>

RUN apt-get update && apt-get upgrade -y && \
	apt-get install -y build-essential git vim emacs

# To build: docker build -t c-env .
# To run: docker run -ti --rm c-env
