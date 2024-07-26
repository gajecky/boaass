FROM node:18-alpine

# Create a non-root user and set the working directory
RUN adduser --disabled-password appuser
WORKDIR /usr/src/app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
USER appuser
RUN npm install

# Copy app code
COPY . .

# Expose port and start the app
EXPOSE 3000
CMD [ "node", "index.js" ]

