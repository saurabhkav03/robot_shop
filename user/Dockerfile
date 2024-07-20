ARG NODE_VERSION=22.4

FROM node:${NODE_VERSION}-alpine 

#ENV NODE_ENV production
ENV INSTANA_AUTO_PROFILE true

WORKDIR /opt/server

COPY package.json /opt/server/

RUN npm install 

COPY . . 

EXPOSE 8080

CMD [ "node", "server.js" ]