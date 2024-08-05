FROM node:18@sha256:11b742eda0142d9ea809fad8c506cbcadb2802c7d4b32e044e6b976691df36b1

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install --verbose
# If you are building your code for production
# RUN npm ci --omit=dev

# Bundle app source
COPY . .

EXPOSE 3000
CMD [ "node", "index.js" ]