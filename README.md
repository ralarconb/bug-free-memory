# bug-free-memory
- Nodejs, MongoDB and Docker integration example.
# Notes
- Connect Nodejs to MongoDB
  - https://youtu.be/qj2oDkvc4dQ?t=1012
- Initialize the project with defaults set to yes.
- Install packages.
- Install development only packages.
- Install mongodb integration package.
- Setup development environment variables.
- Run first time the app.
- Run and test the app.
```sh
npm init -y
npm i express ejs express-ejs-layouts
npm i --save-dev nodemon
npm i mongoose
npm i --save-dev dotenv
npm run devStart
nodemon server.js
```
- Config the .env file
```properties
DATABASE_URL=mongodb://192.168.1.101/mydb
```
- Open the url http://localhost:3000/