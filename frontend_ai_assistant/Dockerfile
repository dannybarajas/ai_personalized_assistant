FROM node:18

# Set Working directory
WORKDIR /app

# Install app dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the app
COPY . .

# Set the host to 0.0.0.0 to allow external access
ENV HOST=0.0.0.0

# Expose the port that Vue's dev server runs on
EXPOSE 5173

# Start the development server
CMD [ "npm", "run", "dev", "--host" ]