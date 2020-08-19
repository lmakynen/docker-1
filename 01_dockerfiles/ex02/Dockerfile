# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lmakynen <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/08/15 18:26:17 by lmakynen          #+#    #+#              #
#    Updated: 2020/08/19 19:38:27 by lmakynen         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ft-rails:on-build

EXPOSE 3000
CMD ["rails", "s", "-b", "0.0.0.0", "-p", "3000"]

# First build an image from your Dockerfile (go to ft-rails for this): docker build -t ft-rails:on-build .
# To build: docker build -t ex02 .
# To run: docker run -it --rm -p 3000:3000 ex02
