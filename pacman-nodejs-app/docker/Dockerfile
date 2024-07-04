FROM node:14

LABEL maintainer="K Hargreaves"

# Create app directory
WORKDIR /usr/src/app

# Clone game source code
RUN git clone https://github.com/wedge22/pacman.git .

# Install app dependencies
RUN npm install

# Use the PORT environment variable or default to 8080
ENV PORT=8080
EXPOSE $PORT

# Run container
CMD ["npm", "start"]