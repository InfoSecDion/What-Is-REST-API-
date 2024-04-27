# -What is REST API?

It is a set of rules that allow programs to talk to each other. The developer creates the API on the server and allows the client to talk to it.

Terminology
API: Application Program Interface
REST: REpresentational State Transfer

Why we use RESTful API?
To expose an independent infrastructure to the outside. Authorized or unauthorized.
To perform operations that require powerful hardware on servers rather than clients.
In order for different applications to communicate with each other with a common data structure.
To ensure the technological independence of clients. (Like Desktop, Mobile, Web, Console, Embedded, etc.)
In order to respond to the needs of different clients with different endpoints. (Like XML, JSON, gRPC etc.)
Data Security

Anatomy Of A Request
Endpoint (Route)
HTTP Method
HTTP Headers
Data (Body / Message)

![image](https://github.com/InfoSecDion/-IOCs-Threat-Detection-In-Yara/assets/105241007/b6e28609-7711-45bf-bbd6-05248e74e622)


![image](https://github.com/InfoSecDion/-IOCs-Threat-Detection-In-Yara/assets/105241007/0c5ff004-abc8-44a6-9da7-4ba587b32147)

Endpoint

It’s a URL that represents our request

Full Path

https://api.ehe.com/users/5/products?name=ehe&price=200

Base URL or Root-Endpoint

https://api.ehe.com/
Path
“:” represents it’s a dynamic value. It can be anything

/users/:userId/products

Request Query

It starts with “?”

That means: I want a certain product with a name and price

?name=ehe&price=200

![image](https://github.com/InfoSecDion/-IOCs-Threat-Detection-In-Yara/assets/105241007/7c931fb0-cf34-41cb-a2d0-d7a4373b83ec)

HTTP Method

HTTP defines a set of request methods to indicate the desired action to be performed for a given resource.

Common Methods (CRUD Methods)

GET, when we want to retrieve our data we should use the GET method.

POST, when we want to create data we should use the POST method.

PUT, when we want to update our data we should use the PUT method.

PATCH, applies partial modifications to a resource.

DELETE, when we want to delete data we should use the DELETE method.

Other Methods

HEAD, is similar toGET request, but without the response body.

CONNECT, establishes a tunnel to the server identified by the target resource.

OPTIONS, describes the communication options for the target resource.

TRACE, performs a message loop-back test along the path to the target resource.

![image](https://github.com/InfoSecDion/-IOCs-Threat-Detection-In-Yara/assets/105241007/fe6d093e-cb0d-484c-b5bc-366a88d670de)

HTTP Headers

it’s a metadata that gives info about the request

Valid headers list

![image](https://github.com/InfoSecDion/-IOCs-Threat-Detection-In-Yara/assets/105241007/379bb303-c682-44be-94e2-024acdd2bfa8)

Data (Body or Message)

It contains the data that you want to send to the server

You can send data only with POST, PUT, PATCH and DELETE requests.

Response Types

Response types comes with API and it briefly tells us what happened there.

Some Example

200: Done, it was okay. Generally, your GETs return this code.

201: “Done, and created.” Generally, your POSTs return this code.

204: “Done, and no body.” Generally, your DELETEs return this code.

400: “Client sent me junk, and I’m not going to mess with it.”

401: “Unauthorized, the client should authenticate first.”

403: “Not allowed. You can’t have it because you logged in but don’t have permission to this thing or to delete this thing.”

404: “Can’t find it.”

410: “Marked as deleted.”
