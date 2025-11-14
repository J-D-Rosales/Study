It's a communication between an app and a service.
>[!note] Definition
>formal agreement between a software provider and a consumer that abstractly communicates how to interact with each other.

The contract has the next document as an agreement
  
```json
Request
  URI: /cashcards/{id}
  HTTP Verb: GET
  Body: None

Response:
  HTTP Status:
    200 OK if the user is authorized and the Cash Card was successfully retrieved
    401 UNAUTHORIZED if the user is unauthenticated or unauthorized
    404 NOT FOUND if the user is authenticated and authorized but the Cash Card cannot be found
  Response Body Type: JSON
  Example Response Body:
    {
      "id": 99,
      "amount": 123.45
    }
```  

The API contracts are written in such a way that can be easily translated into API provider and consumer functionality, and corresponding automated tests.
The response would be generally in Json, instead of XML or YAML. But this are jsut formats. 
DOn't worry about the syntax now, just understand the concepts. 
