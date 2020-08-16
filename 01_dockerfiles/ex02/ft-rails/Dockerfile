# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: lmakynen <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2020/08/15 19:05:25 by lmakynen          #+#    #+#              #
#    Updated: 2020/08/16 20:23:27 by lmakynen         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ruby:2.5.1

MAINTAINER lmakynen <lmakynen@student.hive.fi>

# We need to install SQLite3 database for Rails and Node.js for the applicaton's JavaScript. After that we are installing Rails by using "gem install" command which is provided by RubyGems. I'm using the version 5.2.0 because my example app uses it.

RUN apt-get update && apt-get install -y nodejs sqlite3
RUN gem install rails --version 5.2.0

# Now we are making /opt/app directory which was asked in the subject. We are using -p because it allows us to create sub-directories as well (first it will create the parent directory in case it doesn't exist). We are also changing the working directory there.

RUN mkdir -p /opt/app
WORKDIR /opt/app

# Then we will copy the app folder to /opt/app when the image is being used and built.

ONBUILD COPY app /opt/app

# We are installing dependencies by using bundle and creating a database for the Rails application. With rake db:migrate we will setup the tables in the database. The rake db:seed command loads the data from db/seeds.rb into the database (default data that we want to have in our application for testing purposes). (Rake is a task runner.)

ONBUILD RUN bundle install && \
			rake db:create && \
			rake db:migrate &&\
			rake db:seed
