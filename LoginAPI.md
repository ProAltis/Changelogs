#Login API

The Login API provides a backbone for the gameservers in order to authenticate users.

###Overview


----------


Login API is one of the crucial parts of the Project Altis system, as this validates users are: the correct person, have the correct details and have setup two-factor authentication. 

The Login API is located at https://projectaltis.com/api/ in the root of that folder.

| Variable name      | Info           | Example  |
| ------------- |:-------------:| -----:|
| u      | The players username | Xanon |
| p      | The players password      |   test123 |


The Login API is the only API to use query strings as the input, this is due to the 'outdated' nature of the launcher, so to be backwards compatible, this was kept the same.

A full example would be https://projectaltis.com/api/?u=Xanon&p=test123


###SSL
----------
Requests using SSL are preferred when using the login API due to the sensitive nature of the information. For any kind of official support for your use of the API we will require you to be using a secure connection.

###Response

----------
The Login API like all of our APIs returns a JSON response. 

| Variable name      | Info           | Possible outcomes  |
| ------------- |:-------------:| -----:|
| status      | If the auth was successful | true/false **WARNING! This is a string because @Dubito's launcher** |
| reason      | A message describing the status of the auth      |  'No accounts found with that username!' (for incorrect username and password), 'Please activate two-factor on your account.' (failed),'Welcome back username' (success)  |
| additonal      | Extra information | 'Uh Oh Spaghettios!' (failed message, friendly), The users playtoken |