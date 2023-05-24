# CRUD
* **In your own words, describe what each group of status code represents:**

100’s = These are informational status codes. They tell the client that the header part of the request and that the server will try to fulfill it.

200’s = These are the success codes. They tell the client that the request was accepted.

300’s = These are redirection codes. They tell the client that the resource isn’t available at the location anymore. Could be permanent or temporary.

400’s = These are the client error codes. They are all about invalid requests a client sent to a server.

500’s = These are server error codes. The indicated a problem with the server. Perhaps the server is unreachable, or unavailable, or has too many requests or is down for maintenance.
* **What is a status code 202?** Accepted. The request has been accepted for processing, but the processing has not been completed.
* **What is a status code 308?** Permanent Redirect. This tells the client to use another URL to access the resource and not use the current URL anymore.
* **What code would you use if an update didn’t return data to a client?** 204 No Content.
* **What code would you use if a resource used to exist but no longer does?** 410 Gone.
* **What is the ‘Forbidden’ status code?** 403 Forbidden.
* **Why do we need to pull our MongoDB database string out of our server and put it into our .env?** Because we want to keep it secret and note upload it to github.
* **What is middleware?** Code that runs when the server gets a request but before it gets passed to your routes. The code in middleware has access to the request and response objects and can do things with them.
* **What does app.use(express.json()) do?** It lets our server accept JSON as a body instead of a post element or a query string.
* **What does the /:id mean in a route?** It is a parameter. It is a placeholder for the id of the thing we want to get.
* **What is the difference between PUT and PATCH?** PUT updates all the information for a thing. PATCH updates only the information that is sent to it.
* **How do you make a default value in a schema?** You set the default value in the schema
* **What does a 500 error status code mean?** Something went wrong on the server.
* **What is the difference between a status 200 and a status 201?** A 200 status code means the request was successful. A 201 status code means the request was successful and something was created.