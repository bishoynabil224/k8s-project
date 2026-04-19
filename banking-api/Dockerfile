# Use official Node.js LTS (matches your >=18 requirement)
FROM node:18-alpine

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# Copy only package files first for better caching
COPY package*.json ./

RUN npm install --only=production

COPY . .

EXPOSE 3000

ENV PORT=3000

# Start the app
CMD ["npm", "start"]