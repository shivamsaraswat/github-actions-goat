FROM node:22@sha256:72314283e7a651d65a367f4e72fde18ec431a73ccfc87977f81be5dfc99c1c94

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