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