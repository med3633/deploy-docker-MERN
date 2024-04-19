FROM node:15-alpine

WORKDIR /app

# Copy package.json and package-lock.json first
COPY package*.json ./

# Install dependencies
RUN npm install --legacy-peer-deps

# Copy the rest of the application code
COPY . .

# Build React app into /app/build directory
# RUN npm run build

# Create the ESLint cache directory and adjust permissions
RUN mkdir -p /app/node_modules/.cache/ && chmod -R 777 /app/node_modules/.cache/
# Build React app into /app/build directory
#RUN npm run build
# Expose port
EXPOSE 3000

# Run app
CMD ["npm", "run", "start"]


# FROM node:16-alpine 
# WORKDIR /app

# COPY package*.json ./
# RUN npm ci
# COPY . ./

# ENV PORT 3000
# EXPOSE ${PORT}
# CMD ["npm", "run", "start"]
# # FROM node:15-alpine
# # WORKDIR /app
# # COPY package.json package-lock.json ./
# # RUN npm install --legacy-peer-deps
# # COPY . .

# # # Expose port
# # EXPOSE 3000
# # # Run app
# # 
# # ###