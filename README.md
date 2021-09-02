# Device-Management-App
SPA application is build using Node/React/Mongo and Socket.IO

There are two parts 
- API Layer (Device-Server)
  - Node JS
- Databse (nosql)
  - MongoDB
- FrontEnd (Device-Client)
  - React JS
- Real time event based Client-Server communication
  - Socket IO
- TDD
  - Jest , SuperTest and Enzyme

Steps to run the applications
- Clone the git repo 
  - Go to Device-Management-App/docker-compose.base.yml 
  - Update DBCONSTRING (mongo db connection string .e.g. mongodb+srv://XXXXXX:YYYYYYYYY@AAAAAA.u4d65.mongodb.net/<DBNAME>?retryWrites=true&w=majority)
- Docker should be up and working 
  - Open any Command Prompt , go to the folder and 
  - enter docker-compose build
  - enter docker-compose up
- Open any browser and run the application entering http://localhost:5000 (You can change updating the docker-compose.yml file)
- As per existing config API will run on port 8888.

API Details
- /devices/stats/add
  - To collect and save device specific temperature
- /devices/stats/transactionlist/2021-08-27/2021-09-01
  - Will return MAX and MIN transaction count group by devices for the selected Date Range
- /devices/stats/list/10
  - Will return TOP 10 transactions
  
Nav-Links
- Open the application >> will load the available Device List
- Add Device >> One can add device
- Device List 
  - click on "Check Temperature" button to capture random temperature
  - click on "Add" button to add new device
  - click on "Edit" button to update device info
- Transactions Stats-(Max/Min)
  - Display device name with MAX & MIN transaction count for a duration
- Latest Transactions
  - Render top 10 transaction sort by date&time 
  
NO-refresh
- After add device/update device/delete device/capturing temperature does not require to refresh the page manually. 
- Socket.IO will take care of the auto update on UI.
  
Event queue
- RabbitMQ implementation is not complete
