# Build custom image from node base image.
FROM node

# Run subsequent commands in the app directory.
WORKDIR /app

# Copy everything from this folder into the /app directory
# inside the container file system.
COPY . /app

# Install the node dependencies.
RUN npm install

# When the container is started, expose port 80 to the local machine.
# NOTE: EXPOSE does not actually expose the port automatially. The -p
# option is needed in the 'docker run' command to actually map ports
# in the container to the local machine.
EXPOSE 80

# Overwrite the default executable ran when the image is built.
CMD ["node", "server.js"]
