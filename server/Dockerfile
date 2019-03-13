FROM node:10
WORKDIR /usr/src/app/
COPY . /usr/src/app/
RUN npm cache verify
RUN npm install
COPY . /usr/src/app/
EXPOSE 8080
CMD ["npm", "start"]