#### Status Code ####
A status code is a number that summarizes the response associated to it. There are some common ones,
like 404 for “Page not found,” or 200 for “OK,” or the always helpful 500 for “Internal server error”

These codes are grouped in five sets, based on their meaning:
* 1xx: Information and only defined under HTTP 1.1
* 2XX: The Request is successfully received.
* 3xx: Resource movement from the current location
* 4XX: Source the request did not successfully completed. something wrong.
* 5xx: Server crashed due to some internal error

Source Code | Meaning
------------|------------
200         | OK. Request went fine
201         | Created. Resource created successfully
204         | No content. The action is successful, but empty content as response.
301			| Moved Permanentaly. The resource is moved from the current location moved to another place permanentaly.
400         | Bad Request. request issued some problem. 
401         | Unautherized. When any resource with not able to access with current autherization. 
403			| Forbidden to access the resource.
404			| Not Found. URL is not found in server side.
405			| Method not allowed. The server restricts the resource access and method execution.
500         | Internal Server Error. Generic error code when an unexpected condition met.

[More Details...](http://tools.ietf.org/html/rfc7231#section-6)

[![](https://github.com/shribadiger/RESTFull-API-NodeJS/blob/master/img/button.png)](https://github.com/shribadiger/RESTFull-API-NodeJS/blob/master/Page4.md)
