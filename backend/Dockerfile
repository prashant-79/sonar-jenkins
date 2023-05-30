#  Dockerfile for Node Express Backend

FROM node:10.16-alpine

# Create App Directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Install Dependencies
COPY . .

RUN npm install --silent

#Set ENV
ARG DB_SERVER
ENV DB_SERVER=$DB_SERVER
ARG DB_PORT
ENV DB_PORT=$DB_PORT

# Copy app source code
COPY . .

# Exports
EXPOSE 4000

CMD ["npm","start"]
