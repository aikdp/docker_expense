# #1. It working
# FROM node:20
# EXPOSE 8080
# RUN mkdir /opt/server
# WORKDIR /opt/server
# COPY package.json .
# COPY *.js .
# RUN npm install
# #use container name
# ENV DB_HOST="mysql" 
# CMD ["node", "index.js"]

#2. host network 
FROM node:20
EXPOSE 8080
RUN mkdir /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
#use container name
# ENV DB_HOST="mysql" 
ENV DB_HOST="localhost"
CMD ["node", "index.js"]