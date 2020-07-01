req.params vs req.body
======================
```
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
```

req.body is used to access actual form data that you 'posted'.

req.params is used for route parameters.

<https://stackoverflow.com/questions/54903043/express-req-params-vs-req-body-json/54903178>


# req.params
This property is an object containing properties mapped to the named route “parameters”. For example, if you have the route /user/:name, then the “name” property is available as req.params.name. This object defaults to {}.   

<https://expressjs.com/ko/api.html#req.params>   
```
form(method="post");
```

# req.body
Contains key-value pairs of data submitted in the request body. By default, it is undefined, and is populated when you use body-parsing middleware such as express.json() or express.urlencoded().   

<https://expressjs.com/ko/api.html#req.body>
```
form(method="post");
```
   
   
# req.query   
This property is an object containing a property for each query string parameter in the route. When query parser is set to disabled, it is an empty object {}, otherwise it is the result of the configured query parser.

As req.query’s shape is based on user-controlled input, all properties and values in this object are untrusted and should be validated before trusting. For example, req.query.foo.toString() may fail in multiple ways, for example foo may not be there or may not be a string, and toString may not be a function and instead a string or other user-input.   

<https://expressjs.com/ko/api.html#req.query>
```
form(method="get");
```
