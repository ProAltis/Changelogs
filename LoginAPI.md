#Login API

The Login API provides a backbone for the gameservers in order to authenticate users.

###Overview


----------


Login API is one of the crucial parts of the Project Altis system, as this validates users the correct details.

The Login API is located at https://projectaltis.com/api/login

| Variable name      | Info           | Example  |
| ------------- |:-------------:| -----:|
| u      | The players username | Xanon |
| p      | The players password      |   test123 |


The Login API uses POST

###SSL
----------
Requests using SSL are preferred when using the login API due to the sensitive nature of the information. For any kind of official support for your use of the API we will require you to be using a secure connection.

###Response

----------
The Login API like all of our APIs returns a JSON response. 

| Variable name      | Info           | Possible outcomes  |
| ------------- |:-------------:| -----:|
| status      | If the auth was successful | true/false |
| reason      | A message describing the status of the auth      |  'No accounts found with that username!' (for incorrect username and password) *or* 'Welcome back username' (success)  |
| additonal      | Extra information | 'Uh Oh Spaghettios!' (failed message, friendly) *or* The users playtoken |
