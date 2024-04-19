FROM node:15-alpine

WORKDIR /app

# Copy package.json and package-lock.json first
COPY package*.json ./

# Install dependencies
RUN npm install --legacy-peer-deps

# Copy the rest of the application code
COPY . .
RUN npm run build
# Create the ESLint cache directory and adjust permissions
RUN mkdir -p /app/node_modules/.cache/ && chmod -R 777 /app/node_modules/.cache/
# Expose port
EXPOSE 3000
# Run app
CMD ["npm", "run", "start"]

