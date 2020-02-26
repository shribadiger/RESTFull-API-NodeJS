## API Design Best Practices ##
Some of the basic development standards need to be followed. Hence it easy to manage and modify the APIs.

* **_Developer Friendly_**: developer should not face much issues or difficult while extending or working on API.
* **_Extensibility_**: developer should able to add the new features to the existed APIs without much difficulties.
* **_Up-To-Date documentation_**: Developer should keep the proper API documentation for each development.
* **_Proper Error Handling_**: API exception and error should be handled with Error Responses.
* **_Security_**: Based on the System View. Security aspects should be handled
* **_Scalabilit_**: The ability to scale up and down is something any good API should have to properly provide its services.

#### Transport Language ####
JSON gaining stars as transport language in REST based communication. Here some the advantages
1. _Lightweight_
2. _Human Readable format_
3. _Support Different Data Types_

#### Proper Error Handling ####
This is very important in case of API failure. Client should able to understand and take appropirate action based on the error condition.
* _Phase 1: The development of Client_
* _Phase 2: The client is implemented and being used by end users_

## Architecture of RESTfull API Development ##
* Request Handler: Handle the incoming request
* Pre-Processing Chain: Check the authentication details in coming request and validate the inputs request.
* Route Handler: Validate the request and enrich the request by adding the data required for the request handling component.
* Controller: Resposible to handle the request to perticular resource.
* Model: Resource to handle the incoming request.
* Representation Layer: Representational data will get create for client to view on his/her app. 
* Response Layer: 
