# gateKeeper
Middleware that can be used as part of an access control strategy


## Purpose
The purpose of the gateKeeper function is to look at the request and see if there's a header called x-username-and-password. The expected value is a string that looks like user=ellen&pass=superSecretPassword. The function should parse the value for user and pass from the header, and look for a user with those credentials in the USERS array towards the top of the server.js file. If a user is found, the function should set req.user equal to the user object from USERS. If not, req.user should be undefined or null, depending on how you implement your function. All requests that go through this middleware should have a req.user property, but only requests with valid user credentials should have a user object as the value for req.user.
The /api/users/me route will look for a user object on the request. 
