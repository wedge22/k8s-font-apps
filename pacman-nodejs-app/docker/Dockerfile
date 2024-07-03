FROM node:latest

LABEL maintainer="K Hargreaves"

# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Clone game source code
RUN git clone https://github.com/wedge22/pacman.git .

# Install app dependencies
RUN npm install

# Install OpenTelemetry dependencies
RUN npm install @opentelemetry/api @opentelemetry/sdk-node @opentelemetry/auto-instrumentations-node @opentelemetry/exporter-otlp-grpc

# Expose port 8080
EXPOSE 8080

# Run container
CMD ["npm", "start"]
