FROM node:16-alpine 
WORKDIR /app

COPY package*.json ./
RUN npm ci
COPY . ./
# Build React app into /app/build directory
RUN npm run build
ENV PORT 3000
EXPOSE ${PORT}

# FROM node:15-alpine
# WORKDIR /app
# COPY package.json package-lock.json ./
# RUN npm install --legacy-peer-deps
# COPY . .

# # Expose port
# EXPOSE 3000
# # Run app
# CMD ["npm", "run", "start"]
# ###