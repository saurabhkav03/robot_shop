FROM node

ENV INSTANA_AUTO_PROFILE tue

EXPOSE 8080

WORKDIR /opt/server

COPY package.json /opt/server/

RUN npm install

COPY server.json /opt/server/

CMD [ "node", "server.js" ]