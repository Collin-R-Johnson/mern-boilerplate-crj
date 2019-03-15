#node 10 in minimal linux container called alpine
FROM node:10-alpine
#explicitly create working directory in container
RUN mkdir -p /usr/src/react-client
#set working directory, all future stuff is done here
WORKDIR /usr/src/react-client
#copy package and package_lock.json to working directory
COPY package.json /usr/src/react-client/
COPY package_lock.json /usr/src/react-client/
#get node_modules
RUN npm install 
#now that npm install is run, put everything else in working directory
COPY . /usr/src/react-client/
#runs start command in package.json, create react app for client
CMD ["npm", "start"]