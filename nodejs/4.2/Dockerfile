FROM node:4.2
MAINTAINER Patrik Votocek <patrik@votocek.cz>

# Install deps
RUN apt-get update -yqq
RUN apt-get install ruby -yqq

# Install gem
RUN gem install sass

# Install global node modules
RUN npm install -g gulp

CMD ["node"]
