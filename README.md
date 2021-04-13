# Project-Diamond-Python
 Python Project created for IST 411 at Penn State
App1 | Payload Retriever:
 - Retrieve a JSON payload of data from the Internet via CURL so that it is easier to work within python
 - Use a network socket programming to send programming securely using TLS to the security app so that my data does not become vulnerable 
 - Receive the AES encrypted payload from the message handler so that I can control the data
 - Save the JSON payload to a text file so that it is stored in a reachable format 
 - Log actions pass or fail into MongoDB database with a timestamp so that I can know what elements are being correctly put in the database
 - Unit test so that I can confirm all methods are functional
 - Receive the message so that I know everything went through 

App2 | Security:
 - Receive the secure payload using TLS from the payload receiver so that the payload will be secure when the payload is transferred
 - Hash the JSON payload using HMAC so that I am able to append it to the message of the payload and send it securely to app3
 - Append the hashed JSON payload to the message so that it will be capable to transfer the message to app3
 - Use secure SFTP to send the payload to the object broker
 - Log all workflow actions, pass or fail,  into the activity MongoDB NoSQL database with a timestamp
 - Use Unit tests to confirm all methods are functional

App3 | Object Broker:
 - Receive the payload from app 2 using the SFTP so that the payload will be safe and secure
 - Email the payload using the Threading to an email address so that I am able to execute multiple payloads
 - Transform the JSON message into a python object so that I can compress and use it on pyro python
 - Use Pyro ORB to send and compress the python object to app 4 so that app4 can receive the pyro python object
 - Log all workflow actions pass or fail into the activity MongoDB NoSQL database with a timestamp so that I will know is the actions is pass or fail with the date and        time
 - Use Unit tests to confirm all methods so that I can determine is it functional

App4 | Message Handler:
 - Receive the pyro python object so that I can convert it back to JSON
 - Use the RabbitMQ message Queue in order to communicate and send messages to app1
 - Display the calculated round trip time from app 1
 - Record all workflow actions whether pass or fail into the activity MongoDB NoSQL database with a timestamp
 - Confirm all methods are functional using Unit tests

App5 | Central Logger:
 - Log all requests and put them in a MongoDB database 
 - Method handlers will be present for the pass or fail condition
 - Unit tests are displayed to confirm all methods are functional 





