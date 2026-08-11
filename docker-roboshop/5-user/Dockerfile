FROM node:20
WORKDIR /app
COPY package.json .
COPY *.js .
RUN npm install
EXPOSE 8080
# ENV REDIS_URL='redis://<REDIS-IP-ADDRESS>:6379' \
#     MONGO_URL="mongodb://<MONGODB-SERVER-IP-ADDRESS>:27017/users" \
#     MONGO="true"
CMD [ "node", "server.js" ]