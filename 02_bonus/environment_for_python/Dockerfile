# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lmakynen <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/08/25 19:58:31 by lmakynen          #+#    #+#              #
#    Updated: 2020/08/26 14:37:57 by lmakynen         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu

MAINTAINER lmakynen <lmakynen@student.hive.fi>

RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install -y  python3.6 vim git

CMD bash

# To build: docker build -t python .
# To run: docker run -ti --rm python
