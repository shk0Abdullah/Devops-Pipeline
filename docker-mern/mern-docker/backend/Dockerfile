FROM node:20-alpine 



WORKDIR /app

# Copy package and package lock json files to the container
COPY package*.json ./


RUN npm install
COPY . .

EXPOSE 8000

CMD npm start

