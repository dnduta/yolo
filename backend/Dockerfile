FROM node:14 

RUN mkdir -p /usr/src/app

WORKDIR /usr/src/app

COPY package.json /usr/src/app/

RUN npm install

# Copy app files to image
COPY . /usr/src/app

# Debug directory content
RUN pwd

RUN ls -lrt

EXPOSE 5000

CMD [ "npm", "start" ]
