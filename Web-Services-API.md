API--APPLICATION PROGRAMMING INTERFACE
What is API?
-main participant of all the interactivity
-it is like messenger that takes our request to a system and return a response back to via seamless connectivity.
-we use api in many cases like to get data for a web application or to connect to a remote server that has data like weather that keep changing or to enabl two application to exchange data among each other.
-api not only provide reusablity of code but also uses the concept of abstraction i.e showing functionalities by hiding complexity

Real time examples of API?
-waiter in a resturant taking your order to he chef and bringing back the requested dish
-booking a flight online from various sites like make my trip
-switchboard turning off the tublight just on a single press
-signing up in a shoping site from facebook account(web based)

Different types of API?
-XML/SOAP: both uses XML only
-JAVASCRIPT: forcused around javascript
-RESTful APIs: HTTP protocol used (best for web APIs)

What are CURD operations in api?
-GET-retrives the representation of the resource at a specified URI. it has no side effects on the server
-PUT -updates a resource at a specified URI. it can also used  to create a new resource at a specified URI , if the server allows clients to specify new URIs.
-This method replaces the entire product entity.i.e the client is expected to send a complete representation of the updated product.if one want the partial updates , the PATCH method is prefered .
-POST - creates a new resource  the server assigns the URI for new objecct and return this URI as part of the response mesaage.
-DELETE- deletes a resource at a specified URI.

What is Web Service?

-service available over the web
-enabls communication between application over the web
-provide a std protocol/format for communication


Why we use it?

-platform independent communication
-using web services two diff applications (implementation)can talk to each other and exchange info.


Types of Web Services?

-SOAP(simple object access protocol)
--It is set of protocol/rules/definations that how two applications will talk to each other over the web
--structure of soap message:-
---envelop
---header
---body
--medium:HTTP(POST)
--format:XML

-REST(representation state transfer)
--medium:HTTP(POST,GET,PUT,DELETE...)
--format:XML/JSON/TEXT...


What is WSDL?

Service provider publishes an interface for his web services that describes all attributes of the web services.
This is XML based interface and is called -WEB SERVICES DESCRIPTION LANGUAGE(WSDL)
(e.g. online wsdl)


What is UDDI?

A web service provider publishes his web service (through wsdl) on an online directory from where consumers can query and search the web services. 
This online registry / directory is called- UNIVERSAL DESCRIPTION DISCOVERY AND INTEGRATION(UDDI)
Is an XML based std for publishing and finding web sevices.


What are SOAP Web services?

A web service that compiles to the SOAP web services specifications is a SOAP web service.
W3 defines and didicates this stds.
SOAP WEB SERVICES SPECIFICATIONS
-BASIC
--SOAP 
--WSDL
--UDDI
-EXTENDED
--WS-SECURITY
--WS-POLICY
--WS-I


What are RESTful web services?
--it is an architectural style
--it define set of principles to be followed while designning a service for communication/data exchange between 2 applications
--when these principles are applied while designing web services (for client - server interaction) we get RESTful web services.
--principles to guide how the data/info (state) of a resource is transferred using representation.
--developed by-ROY FIELDING-2000

what are the principles/constraints of restfull architectur:
1. Uniform interface 
--Resource: everything is a resource
--URI: any resources/data can be accesed by a URI(uniform resource identifier)
--HTTP: make explicit use of HTTP methods
		--POST C-CREATE
		--GET  R-READ
		--PUT  U-PUT
		--DELETE D-DELETE
2. stateless
--all client server communication are stateless
--each request from the client to the server must contain all of the data that is necessary to handle the request
--no need of storing any state on the server
eg. everytime currnt state of a cart should be sent to server
3. Cacheable
--happens at cient side
--the response send by the server not only contain the data but also some meta data which shows whether to store  response locally or not
4. Layered System
--layers can exist between client and server
--there are many layers between client and server
--these are http intermediaries
--can be used for mesaage translation/improving performance with caching 
--can include proxies and gateway
--there is also caching layer inbetween eg. if a request come from a client within an hour and there is no change in resource then the same response can again send to client without going to server
--this improves scaliblity
5. Code On Demand(optional)
--ability to download and execute code on client side


Introduction to POSTMAN for API development:

-Postman is an API development tool which helps to build , test,modify APIs.Almost any functionality that could be needed by any developer is encapsulated in this tool. It has ability to make various types of HTTP requests (GET,POST,PUT,DELETE,PATCH) , saving environments for later use, converting APIs for various languages(like javascript,python).
-software environment:
--the longest middle input field that looks something like a search bar is where the url that we want to GET , POST,DELETE,etc is fed.
--just to the left of it , is a drop down button which has all the various http methods as options.
--to the right of it is the params button.if you click on it , a new interface will appear.params are basically the data we want to send to the server with our request.
--to the left of this button is the send button which is used in sending the request to the server or the app in this case.

-explanations of header:
--connection:this shows the status of connection it can be keep-alive which means the connection are still active

