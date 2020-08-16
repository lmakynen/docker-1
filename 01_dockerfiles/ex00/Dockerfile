# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lmakynen <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/08/12 18:32:24 by lmakynen          #+#    #+#              #
#    Updated: 2020/08/12 18:41:38 by lmakynen         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM alpine

MAINTAINER lmakynen <lmakynen@student.hive.fi>

RUN apk update && apk upgrade && apk add vim

ENTRYPOINT vim

# You can build it by typing: docker build -t ex00 .
# You can run it by typing: docker run --rm -ti ex00
