# bug-free-memory
- Nodejs, MongoDB and Docker integration example.
# Config images
- Pull mongodb
- Pull mongo express
- Create mongo network
- Run mongo db on mongo network
- Run mongo express on mongo network
- Check mongo express on http://192.168.1.101:8081
- Create a mongo database (mydb) on mongo server using mongo express
```sh
docker pull mongo
docker pull mongo-express
docker network create mongo-network
docker run -d \
 -p 27017:27017 \
 -e MONGO_INITDB_USERNAME=admin \
 -e MONGO_INITDB_PASSWORD=password \
 --name mongodb \
 --net mongo-network \
 mongo 
docker run -d \
  -p 8081:8081 \
  -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin \
  -e ME_CONFIG_MONGODB_ADMINPASSWORD=password \
  --net mongo-network \
  --name mongo-express \
  -e ME_CONFIG_MONGODB_SERVER=mongodb \
  mongo-express
```
# Build the app
- Initialize the project with defaults set to yes.
- Install packages.
- Install development only packages.
- Install mongodb integration package.
- Setup development environment variables.
- Run first time the app.
```sh
npm init -y
npm i express ejs express-ejs-layouts
npm i --save-dev nodemon
npm i mongoose
npm i --save-dev dotenv
npm run devStart
```
- Config the .env file
```properties
DATABASE_URL=mongodb://192.168.1.101/mydb
```
- Open the url http://localhost:3000/
# Setup
- Clone the app
```sh
git clone https://github.com/ralarconb/bug-free-memory.git
cd bug-free-memory
```
# Notes
- Run and test the app.
```sh
nodemon server.js
```