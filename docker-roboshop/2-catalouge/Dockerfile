FROM node:20
WORKDIR /app
COPY package.json .
COPY *.js .
RUN npm install
# ENV MONGO_URL="mongodb://<MONGODB-SERVER-IPADDRESS>:27017/catalogue"
#In docker docker container names used as a DNS, hence in place of mongodb ip adress, we use mongodb container name
ENV MONGO_URL="mongodb://mongodb:27017/catalogue" \
    MONGO="true"
CMD ["node", "server.js"]