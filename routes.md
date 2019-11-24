# API routes

This document contains a list of all defined api routes of xenia services, along with the expected/enforced contents of the json requests and responses. Note all payloads may be padded with extra security or loggging heading that will be determined later. 

## rock 
### /user_init
* Request payload:
	`username: string (user name for new user)`
	`email: string (email for new user)`
	`password: string (password for new user)`
	
	All fields are required 

* Response payload
	`result: bool (true if user account creation successful)`
	`message: None or String (None if result is True, otherwise error message)`  

### /update_user
* Request payload 
	`username: string (user that is having the update)`
	todo, will update when data model is finalized 

* Response payload
	`result: bool (true if user account creation successful)`
	`message: None or String (None if result is True, otherwise error message)` 

### /login
* Request payload
	`username: string (current user)`
	`password: string (current password)`

* Response payload
	`result: bool (true if user account creation successful)`
	`token: JWT or None (if result login successful user token will be here`
	`message: None or String (None if result is True, otherwise error message)`
		