req.params vs req.body

/* fetch all users */
GET /users 

/* fetch specific user */
GET /users/:userId

/* create new user */
POST /users 

/* edit specific user */
PUT /users/:userId

/* delete specific user */
DELETE /users/:userId


req.body is used to access actual form data that you 'posted'.

req.params is used for route parameters, in your case userId which is passed in the parameters:

// https://stackoverflow.com/questions/54903043/express-req-params-vs-req-body-json/54903178


req.params
This property is an object containing properties mapped to the named route “parameters”. For example, if you have the route /user/:name, then the “name” property is available as req.params.name. This object defaults to {}.

req.body
Contains key-value pairs of data submitted in the request body. By default, it is undefined, and is populated when you use body-parsing middleware such as express.json() or express.urlencoded().