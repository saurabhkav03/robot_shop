ARG NODE_VERSION=22.4

FROM node:${NODE_VERSION}-alpine

ENV INSTANA_AUTO_PROFILE true 

EXPOSE 8080

WORKDIR /opt/server

COPY package.json /opt/server/

RUN npm install 

COPY . .

CMD [ "node", "server.js" ]