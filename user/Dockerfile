FROM node:14

#ENV NODE_ENV production
ENV INSTANA_AUTO_PROFILE true

WORKDIR /opt/server

COPY package.json /opt/server/


RUN npm install 

COPY user/server.js /opt/server/

EXPOSE 8080

CMD [ "node", "server.js" ]