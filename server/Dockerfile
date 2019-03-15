#node 10 in minimal linux container called alpine
FROM node:10-alpine
#explicitly create working directory in container
RUN mkdir -p /usr/src/server-app
#explicitly create working directory in container
WORKDIR /usr/src/server-app
#copy package and package_lock.json to working directory
COPY package.json /usr/src/server-app/
COPY package_lock.json /usr/src/server-app/
#get node_modules
RUN npm install
#now that npm install is run, put everything else in working directory
COPY . /usr/src/server-app/
#runs start command in package.json, create react app for client
CMD ["npm", "start"]