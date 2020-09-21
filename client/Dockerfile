FROM node:14 

RUN mkdir -p /usr/src/app

WORKDIR /usr/src/app

COPY package.json /usr/src/app/

RUN npm install

# Copy src files to image
COPY . /usr/src/app

# Debug show directory content
RUN pwd

RUN ls -lrt

RUN npm run build

RUN npm install -g serve

EXPOSE 3000

CMD [ "npm", "start" ]
