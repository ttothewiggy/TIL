 ### REST API LinkdIn leanring Course

 ## Representational State Transfer Application Programming Interface

 - REST and API are acronyms for Representational State Transfer and Application Programming Interface.
 - URI =  Universal Resource Identifier request. 
 - An API is a set of features and rules that exist inside a software program enabling interaction between the software and other items, such as other software or hardware. In the context of REST APIs, the API is the collection of tools used to access and work with REST resources through your adverbs including get, pulls, put, and delete. You can think of the REST resource as a librarian and the API as the language used to talk to them. 
 - The URL, or Universal Resource Locator, is a subset of the URI. 

 ### The 6 Constraints of REST

 1. Client-Server Architecture - The client manages user interface concerns while the server manages data storage concerns. Highly portable.  1 REST service can serve many different clients. 
 2. Statelessness - No client context or information, aka "state, can be stoed on the server beteween requests. 
 3. Cacheability -  All REST responses must eb clearly marked as cacheable or not cacheable. 
 4. Layered System - The client cannot know, and shouldnt care, whether it's connected directly to the server or to an intermediary like a CDN or mirror. 
 5. Code on Demand - Servers are allowed to transfer executable code like JS and compiled components to clients. 
 6. Uniform Interface 
 6.1 Resource identification in requests - The URI request must specify what resource it is looking for and what format the resposnse should use. 
 6.2 Resource manipulation through representations - Once a client has a representation of a resource, it can modify or delete the resource. 
 6.3 Self descriptive messages - Each representatoinoin must describe it's own format. 
 6.4 Hypermedia as the engine of application state - Once a client has access to a REST service, it should be able to discover all available resources and methods thourgh the hyperlinks provided. 

 ### Who or What interacts with REST API's

 Communication with the REST API is handled by the client, which can be anything, really. A website, an app, even an internet of things device. The REST API does not care. It just receives requests, processes data, and sends responses, and all that data is consumed by the REST client.