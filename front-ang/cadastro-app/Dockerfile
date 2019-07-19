FROM node:10.16.0-alpine as node

# Create a directory where our app will be placed
RUN mkdir -p /usr/src/app

# Change directory so that our commands run inside this new directory

WORKDIR /usr/src/app

# Copy dependency definitions

COPY package*.json /usr/src/app/

# Install dependecies
RUN npm install -g @angular/cli

RUN npm install

# Get all the code needed to run the app

COPY . /usr/src/app

EXPOSE 4200

CMD ng serve --host 0.0.0.0