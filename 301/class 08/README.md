#  APIs

* **What does REST stand for?** Representational State Transfer
* **REST APIs are designed around a ____.** Resource
* **What is an identifier of a resource? Give an example.** Any resource has an identifier which is an uri that uniquely identifies that resources for example
* **What are the most common HTTP verbs?** GET, POST, PUT, PATCH, and DELETE
* **What should the URIs be based on?** URIs should be based on nouns(the resource) and not the verbs(the operations on the resource)
* **Give an example of a good URI.** https://adventure-works.com/orders the endpoint is all just describes the resource and not the operation
* **What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?** A chatty API exposes many small resources instead of larger chunks which can cause the client to make more request and put a heavier load on your server.
* **What status code does a successful GET request return?** 200 (OK)
* **What status code does an unsuccessful GET request return?** 404 (Not Found)
* **What status code does a successful POST request return?** 201 (Created)
* **What status code does a successful DELETE request return?** 204(No Content)