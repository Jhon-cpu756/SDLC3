#FROM NODEJS
FROM node:23.9.0-alpine

# make the 'app' folder the current working dir
RUN mkdir front
COPY . /front
WORKDIR /front

# install project dependencies
RUN npm cache clean –force

RUN apk update 
RUN apk add net-tools
RUN npm install

EXPOSE 3001
CMD ["npm", "run", "dev"]