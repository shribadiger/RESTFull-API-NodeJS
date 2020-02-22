### Content Negotiation ###
Header information will contains the Content types. 
```
Accept: text/html; q=1.0, text/*; q=0.8, image/gif; q=0.6, image/jpeg; q=0.6, image/*;
q=0.5, */*; q=0.1
```

At the server side, It will validate the type which is going to represent. It acts the functionality based on type which present. 

#### Using the File Extention ####
The extension portion of the file’s name indicates the content type to the operating system and any
other software trying to use it; so in the following case, the extension added to the resource’s URL (unique
identifier) indicates to the server the type of representation wanted.

```http
GET /api/v1/books.json
GET /api/v1/books.xml
```
#### Resource Identification ####
This is provided by the full path of the resource present in server side. (Unique Resource Identification).
**Example:** 
```http
GET /api/v1/books/computer_science/operating-system
GET /api/v1/books/computer_science/network-security
```

#### Actions ####
HTTP verbs are properly matched with some of action. The following table indicates about the action associated with each verbs.

HTTP Verb | Actions
----------|---------
GET       | Access a resource in a read-only mode.
POS       |used to send a new resource into the server (create action).
PUT       | used to update a given resource (update action).
DELETE    | used to delete the resource
HEAD      | Not part of the CRUD actions, but the verb is used to ask if a given resource exists without returning any of its representations.
OPTIONS   | Not part of the CRUD actions, but used to retrieve a list of available verbs on a given resource (i.e., What can the client do with a specific resource?).

#### Complex Actions ####
Some of complex oparations will be mentioned in URI to perfrom at server side. following example will indicates complex operations. 
```http
GET /api/v1/blogpost/12342/like
GET /api/v1/books/search
GET /api/v1/authors/filtering
```
**Advanced Complex Actions**
```http
PUT /api/v1/blogposts/12342?action=like
GET /api/v1/books?q=[SEARCH-TERM]
GET /api/v1/authors?filters=[COMMA SEPARATED LIST OF FILTERS]
```
**Hyepermedia Information in Response and Main Entry Point**
*Example:*
```json
{
"metadata": {
"links": [
"books": {
"uri": "/books",
"content-type": "application/json"
},
"authors": {
"uri": "/authors",
"content-type": "application/json"
}
]
}
}
```
*Extended Example*
```json
{
  "resources": [
   {
      "title": "Harry Potter and the Half Blood prince",
      "description": "......",
      "author": {
      "name": "J.K.Rowling",
      "metadata": {
            "links": {
                  "data": {
                      "uri": "/authors/j-k-rowling",
                       "content-type": "application/json"
                          },
                  "books": {
                      "uri": "/authors/j-k-rowling/books",
                      "content-type": "application/json"
                            }
                       }
                  }
        },
      "copies": 10
      },
{
    "title": "Dune",
    "description": "......",
    "author": {
          "name": "Frank Herbert",
          "metadata": {
                "links": {
                    "data": {
                          "uri": "/authors/frank-herbert",
                          "content-type": "application/json"
                            },
                    "books": {
                           "uri": "/authors/frank-herbert/books",
                             "content-type": "application/json"
                              }
                          }
                      }
                },
      "copies": 5
  }
],
"total": 100,
"metadata": {
        "links": {
            "next": {
                "uri": "/books?page=1",
                "content-type": "application/json"
                    }
                  }
              }
}
```
