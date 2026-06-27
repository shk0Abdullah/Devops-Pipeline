FROM node:20-alpine 

# Create a user with the permissions to run the app 
# -S creates a system user
# -G assigns the user to a group
# app is the name of the user and the group
# its a good practice to run the app as a non root user

RUN addgroup app && adduser -S -G app app


# set the user to run the app
USER app


WORKDIR /app

# Copy package and package lock json files to the container
COPY package*.json ./

USER root


RUN chown -R app:app .

USER app

RUN npm install
COPY . .

EXPOSE 5173

CMD npm run dev

