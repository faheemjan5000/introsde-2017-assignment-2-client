# introsde-2017-assignment-2-client
Client code done by
Name : Main muhammad faheem - Jan  
Email : main.jan@unitn.it  

Server Code done by  
Name : Danish Asghar - Cheema  
Email : danishasghar.cheema@unitn.it  

Server heroku Base ULR: https://introsde-asgn2-server.herokuapp.com  
Server Git ripo: https://github.com/danishc/introsde-2017-assignment-2-server  

Client Git riop: https://github.com/faheemjan5000/introsde-2017-assignment-2-client  
                 

### About the Code:

I created one Client Class named as "Client" which has some attributes, methods and main method defined.   
like getting a person by id, updating person,deleting person, printing activities etc etc.there is one other class named as "SysStreamsLogger.java" which do all the actions needed to log things. there is one log file which   
has all the ouput saved.there is the Build file which has all the targets written and ivy.xml file which has different  
dependencies needed for my project.    

### Tasks the Code do :    

`STEP 1. Print URL of the server you are calling` //prints the URL of the server      
`STEP 3.1 XML => Request #1 GET BASE_URL/person Accept: APPLICATION/XML` //Calculates total number of people using GET request.    
 and accept response in xml formate.If more than 4, result is OK, else is ERROR (less than 5 persons).    
 Saves into a variable id of the first person (first_person_id) and of the last person (last_person_id).   
`STEP 3.1 JSON => Request #1 GET BASE_URL/person Accept: APPLICATION/JSON` // same as above but in JSON format.    
`STEP 3.2 XML => Request #2 GET /person/101 Accept: APPLICATION/XML` //gets person with id 101 in xml format.    
`STEP 3.2 JSON => Request #2 GET /person/101 Accept: APPLICATION/JSON`//same result as above but in JSON format.    
`STEP 3.3 XML => Request #3 PUT /person/101 Accept:APPLICATION/XML Content-type:APPLICATION/XML` // updates the person with id 101.    
`STEP 3.3 JSON => Request #3 PUT /person/101 Accept:APPLICATION/JSON Content-type:APPLICATION/JSON`// same result as above but in    
JSON format.    
`STEP 3.4 XML => Request #4 POST /person Accept:APPLICATION/XML Content-type:APPLICATION/XML`//creates a new person with one activity    preference.  
`STEP 3.4 JSON => Request #4 POST /person Accept:APPLICATION/JSON Content-type:APPLICATION/JSON`//same result as above but in JSON     format.    
`STEP 3.5 DELETE /person/{id} Accept:APPLICATION/XML Content-type:APPLICATION/XML` //it deletes the person identified by {id}    
from the system.  Http status code :204=> Request #2 GET /person/106 Accept: APPLICATION/XML if it return 404 result is OK  
=> Result: OK     
`Step 3.6 XML => Request #6 GET /activity_types Accept:APPLICATION/XML` //it returns the list of activity_types my model supports.   
`Step 3.6 JSON => Request #6 GET /activity_types Accept:APPLICATION/JSON`//same result as above but in json format.    
`Step# 3.7 XML => Request#7 (GET BASE_URL/person/{id}/{activity_type})`//it returns the list of activities of {activity_type} for a   person with given id.but first  it checks if the person have atleast one activity.  
`Step# 3.7 JSON => Request#7 (GET BASE_URL/person/{id}/{activity_type})`// same result as above but in json format.    
`STEP 3.8 XML  => GET /person/{id}/{activity_type}/{activity_id} Accept:APPLICATION/XML`// it returns the activities of {activity_type}   (e.g. Social) identified by     {activity_id} for person identified by {id}.    
`STEP 3.8 JSON  => GET /person/{id}/{activity_type}/{activity_id} Accept:APPLICATION/JSON`//same result as above but in json format.     
`Step# 3.9 XML => Request #9 => POST /person/101/WorkMeeting Accept:APPLICATION/XML Content-Type:APPLICATION/XML` //it saves a new   value for the {activity_type} (e.g. Social) of person identified by {id} and archive the old value in the history.    
`Step# 3.9  JSON => Request #9 => POST /person/101/Sport Accept:APPLICATION/JSON Content-Type:APPLICATION/JSON` //same result as  
above but in json format.    
`STEP 3.10: XML PUT /person/{id}/{activity_type}/{activity_id}`// it updates the value for the {activity_type}  
(e.g., Social) identified by {activity_id}, related to the person identified by {id} in xml format.    
`STEP 3.10: JSON PUT /person/{id}/{activity_type}/{activity_id}`//same result as above but in json format.    
`STEP#11 : XML GET /person/{id}/{activity_type}?before={beforeDate}&after={afterDate}`//it return the activities of {activity_type}     (e.g., Social) for person {id} which {start_date} is in the specified range of date.    
 `STEP#11 : JSON GET /person/{id}/{activity_type}?before={beforeDate}&after={afterDate}`// same result as above but in json format.     
                  
### execuation
1) clone or download the code
2) make sure to change the BASEURL in Client class if your server Url is diffent from the one given the link above.
from the project directory run the following command. it will generate new log file.
```
ant execute.client
```

