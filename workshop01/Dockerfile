FROM node:latest

ENV APP_PORT=3000 APP_DIR=/app DB_HOST=mydb DB_PORT=3306 DB_USER=root DB_PASSWORD=changeit

WORKDIR ${APP_DIR}
ADD package.json .
ADD package-lock.json .
RUN npm install

ADD public public
ADD views views
ADD config config
ADD main.js .


EXPOSE ${APP_PORT}

ENTRYPOINT ["node", "main.js"]
CMD ["$APP_PORT"]