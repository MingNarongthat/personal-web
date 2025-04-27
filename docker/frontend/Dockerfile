# Build stage
FROM node:18-alpine AS builder

WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy source code
COPY . .

# Build the application
RUN npm run build

# Production stage
FROM node:18-alpine

WORKDIR /app

# Copy built application
COPY --from=builder /app/.output ./
COPY --from=builder /app/.nuxt ./
COPY --from=builder /app/package*.json ./

# Install production dependencies
RUN npm install --production

# Expose port
EXPOSE 3000

# Start the application
CMD ["node", ".output/server/index.mjs"]
