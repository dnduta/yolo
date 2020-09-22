FROM node:14-alpine 

RUN mkdir -p /app

WORKDIR /app

ENV PATH /app/node_modules/.bin:$PATH

COPY package.json .

COPY package-lock.json .

RUN npm install --no-optional

# Copy app files to image
COPY . .

# Debug directory content
RUN pwd

RUN ls -lrt

EXPOSE 5000

CMD [ "npm", "start" ]
