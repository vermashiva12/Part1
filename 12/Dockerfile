FROM ubuntu:16.04

WORKDIR /webapp

# install dependencies
RUN apt-get update && apt-get install -y curl git-core

# Install node/npm
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get update && apt-get install -y nodejs

# Check the installation of node/npm
RUN node -v
RUN npm -v

# Install the application.
RUN git clone https://github.com/docker-hy/material-applications/example-frontend.git



# Expose the port
EXPOSE 5000

# Setup depedencies
RUN cd example-frontend && npm install

# When container is started start node
CMD cd example-frontend && npm start
