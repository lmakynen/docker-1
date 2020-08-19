# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lmakynen <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/08/17 17:43:00 by lmakynen          #+#    #+#              #
#    Updated: 2020/08/19 19:18:16 by lmakynen         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian

MAINTAINER lmakynen <lmakynen@student.hive.fi>

# We are installing and configuring necessary dependencies. cURL is a command-line tool for getting or sending data including files using URL syntax. OpenSSH is the premier connectivity tool for remote login with the SSH protocol. Postfix is an open-source mail transfer agent (MTA) that routes and delivers electronic mail.

RUN apt-get update && apt-get upgrade -y && \
	apt-get install -y curl openssh-server ca-certificates postfix

# We are adding the GitLab package repository and installing the package.
# -S,--show-error = Show error, make curl show errors when they occur. -s,--silent = Silent mode (don't output anything).

RUN curl -sS https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.deb.sh | bash

RUN apt-get install gitlab-ce

EXPOSE 22 80 443

# We are starting the SSH service and after that we will manually start the GitLab and reconfigure the ctl. With gitlab-ctl tail we are viewing live log updates of GitLab logs. 

ENTRYPOINT service ssh start && (/opt/gitlab/embedded/bin/runsvdir-start &) && gitlab-ctl reconfigure && gitlab-ctl tail

# To build: docker build -t ex03 .
# To run: docker run -it -p 8080:80 -p 8022:22 -p 8443:443 --privileged ex03
# Then you can access GitLab from browser by typing <ip>:8080
