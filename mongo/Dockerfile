FROM mongo

COPY mongo/users.js /docker-entrypoint-initdb.d/
COPY mongo/catalogue.js /docker-entrypoint-initdb.d/

CMD [ "mongod" ]