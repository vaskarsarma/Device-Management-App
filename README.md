# Device-Management-App
Application is build using Node/React/Mongo and Socket.IO

There are two parts 
- Service Layer (Device-Server)
  - Node JS
  - MongoDB
  - Socket IO
- FrontEnd (Device-Client)
  - React JS

Steps to run the applications
- Close this git repo 
- Go to docker-compose.base.yml 
  - update DBCONSTRING (mongo db connection string .e.g. mongodb+srv://XXXXXX:YYYYYYYYY@AAAAAA.u4d65.mongodb.net/<DBNAME>?retryWrites=true&w=majority)
- Docker should be up and working 
- Open any Command Prompt , go to the folder and 
  - enter docker-compose build
  - enter docker-compose up
  - Open any browser and run the application entering http://localhost:3000
  
  
  
 
  
