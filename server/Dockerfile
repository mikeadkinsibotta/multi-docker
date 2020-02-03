# Get the node image using the alpine 
FROM node:alpine
# Set the working directory in the container
WORKDIR '/app'
# Copy over package.json to the container from our app folder
COPY ./package.json ./
# Install all the dependenices
RUN npm install
# Copy everything else over
COPY . .
# Set the default commmand for when the container starts.
CMD npm run dev
