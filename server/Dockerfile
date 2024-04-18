# FROM node:16-alpine 
# WORKDIR /app
# COPY package*.json ./
# RUN npm ci
# COPY . ./
# ENV PORT 3700
# EXPOSE ${PORT}
FROM node:16-alpine

RUN mkdir -p /home/node/app/node_modules && chown -R node:node /home/node/app

WORKDIR /home/node/app

COPY package*.json ./

# Change ownership of package-lock.json
RUN chown node:node package-lock.json

USER node

# Install npm packages
RUN npm install --force

COPY --chown=node:node . .

EXPOSE 3700