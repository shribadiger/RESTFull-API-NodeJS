# Rest API Development in Node JS
### INDEX ###
* [Introduction](https://github.com/shribadiger/RESTFull-API-NodeJS/blob/master/README.md)
* [Content Negotiation](https://github.com/shribadiger/RESTFull-API-NodeJS/blob/master/page2.md)
* [Status Code](https://github.com/shribadiger/RESTFull-API-NodeJS/blob/master/page3.md)
* [API Design Best Practices](https://github.com/shribadiger/RESTFull-API-NodeJS/blob/master/page4.md)

REST -- Representational State Transfer. 
It is an architectural design style for distributed systems.

### How Rest API helps in improvement of distributed system
<li> Performance: efficient and simple implementation</li>
<li> scalability of component interaction</li>
<li> Simplicity of Interface</li>
<li> Modification of component</li>
<li> Portability</li>
<li> Reliability because of stateless constraint</li>
<li> Visibility</li>

### REST Constraints:
- **Client-Server Architecture** : The main principle is "separation of concern". Server will be in
                                charge to handle the request from the client. The client and server code
                                is independent. The change in the Client or Server will not impact on each other.
- **Stateless:** Communication between client and server must be stateless, meaning that each request done from the client must have all the information required for the server to understand it, without taking advantage of any stored data.
- **Cacheable:** By caching the responses, there are some obvious benefits that get added to the architecture: on the server side, some interactions (a database request, for example) are completely bypassed while the content is cached. On the client side, an apparent improvement of performance is perceived.
- **Uniform Interface:** In order to achieve the uniform interface, a new set of constraints must be added to the interface:identification of resources, manipulation of resources through representation, self-descriptive messages, and hypermedia as the engine of application state (a.k.a HATEOAS). I’ll discuss some of these constraints shortly.

### Resources:
- Services which are provided.
- Information changes between the parties.
- Action which are going to perform in server side.

**Resource Structure**

Property | Description
---------|------------
Representation | JSON, XML - How the data getting represented in process
Identification | URL - one specific resource at a time
Metadata | content type, modification time, any other control information
Control Data | cache-control information for further processing
----------|----------

- *Representation* :
    ``` js
    { "name":"Shrikant Badiger",
      "ID" : 12345,
      "Location":"Bangalore" 
    }
    ```
[![](https://github.com/shribadiger/RESTFull-API-NodeJS/blob/master/img/button.png)](https://github.com/shribadiger/RESTFull-API-NodeJS/blob/master/Page2.md)
