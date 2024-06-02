FROM ubuntu:22.04

EXPOSE 5000

RUN apt-get update -y && apt-get install curl -y

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash

RUN apt-get install nodejs -y

COPY . .
 
RUN npm install

RUN npm run build && npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]
