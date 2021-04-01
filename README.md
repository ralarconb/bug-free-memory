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
- Run the app.
```sh
npm init -y
npm i express ejs express-ejs-layouts
npm i --save-dev nodemon
npm i mongoose
npm i --save-dev dotenv
nodemon server.js
```
- Add development and production mode initializing scripts.
- http://localhost:3000/