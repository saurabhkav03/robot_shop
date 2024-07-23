FROM node

ENV INSTANA_AUTO_PROFILE true

EXPOSE 8080

WORKDIR /opt/server

COPY cart/package.json /opt/server/

RUN npm install

COPY cart/server.js /opt/server/

CMD [ "node", "server.js" ]