FROM node:0.12
MAINTAINER Patrik Votocek <patrik@votocek.cz>

# Install deps
RUN apt-get update -yqq
RUN apt-get install imagemagick ruby -yqq

# Install gem
RUN gem install sass

# Install global node modules
RUN npm install -g gulp

CMD ["node"]
