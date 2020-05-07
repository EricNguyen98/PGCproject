# PGCproject
#### This is a Web App for INST377
#### This project aims to make the PG County Offices dataset queryable and useable to UMD undergraduates.
#### Application Link: https://pgcgovofficesfinalproject.herokuapp.com/ 

### Target Browsers: Desktop(Chrome), Mobile
### User Manual: [Click to go to the User Manual](/docs/user.md)
### Developer Manual:  [Click to go to the User Manual](#developer-manual)


## Developer Manual
#### The application has the capability to run locally.
#### Download the repo to your machine and run 'npm install' in the folder
#### Run the command 'npm start' and the application will run locally on 3000.
#### Server will be using files in the public folder, to change see line 13 in server.js in the main folder. 
#### No formal tests have been written 
### API: 
#### All end points are expecting a JSON object/ form object with the key agency and an agency bound to that key. Only end point that does not rely on the input is the GET route. 
#### Example of JSON object: { agency: 'FIRE' } will cause endpoints to read the agency as FIRE. Key must be 'agency'. Value is not case sensitive. FiRE or fire or any case variation will still be read as FIRE. 
#### GET is used to get all offices and return that to the list and map. Returns all offices in a JSON object un filtered.
#### PUT is used to populate the list of offices with offices of interest based on agency. Returns a filtered JSON object with office: description, address, city, agency.
#### POST is used to get all offices of interest and return information needed to generate map points.  Returns a filtered JSON object with office: description, address, city, agency, longitude, latitude. POST includes long and lat PUT does not. 

#### Bugs: CSS animations occasionally leave a one pixel fragment

#### Roadmap: Clean up artifacts in code from development and optimize code. Write tests and improve useablity of app. If more endpoints added, split API rounter to separate file in server_files folder.
