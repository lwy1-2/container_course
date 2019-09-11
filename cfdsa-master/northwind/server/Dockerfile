# select the base image
FROM node:latest

LABEL name='LWY'
LABEL maintainer='lwy@yahoo.com.sg'

# explain mydb 
ENV DB_HOST=mydb
ENV DB_PORT=3306
ENV APP_PORT=3000
ENV APP_DIR=/app

WORKDIR ${APP_DIR}

ADD package.json .
ADD package-lock.json .
ADD main.js .
ADD config config
ADD public public
ADD views views

#INSTALL Dependency
RUN npm install

#Expose the port 
EXPOSE ${APP_PORT}

#start the app
ENTRYPOINT [ "node", "main.js" ]

#CMD 