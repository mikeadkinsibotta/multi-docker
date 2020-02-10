# Get the node image using the alpine 
FROM node:alpine as builder
# Set the working directory in the container
WORKDIR '/app'
# Copy over package.json to the container from our app folder
COPY ./package.json ./
# Install all the dependenices
RUN npm install
# Copy everything else over
COPY . .
# Set the default commmand for when the container starts.
CMD npm run start

FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /app/build /usr/share/nginx/html

 