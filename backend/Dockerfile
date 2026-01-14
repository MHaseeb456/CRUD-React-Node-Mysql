# Use official Node.js LTS
FROM node:16-bullseye

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json first
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy rest of the app
COPY . .

# Copy .env if you have it
# (optional: remove this line if you pass env vars via docker run)
COPY .env.example .

# Expose port 3000 because your index.js uses process.env.PORT || 3000
EXPOSE 3000

# Start the app
CMD ["node", "index.js"]
