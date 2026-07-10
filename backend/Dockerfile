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

# #2. host network 
# FROM node:20
# EXPOSE 8080
# RUN mkdir /opt/server
# WORKDIR /opt/server
# COPY package.json .
# COPY *.js .
# RUN npm install
# #use container name
# # ENV DB_HOST="mysql" 
# ENV DB_HOST="localhost"
# CMD ["node", "index.js"]


#3. best practices
FROM node:20.18.0-alpine3.20
EXPOSE 8080
ENV DB_HOST="mysql"
RUN addgroup -S expense && adduser -S expense -G expense
RUN mkdir /opt/server
RUN chown -R expense:expense /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
USER expense
#use container name
CMD ["node", "index.js"]