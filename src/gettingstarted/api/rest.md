# REST API

## Endpoints

To create your own REST API endpoints for an app, create a class that inherits from the **AppsDock &#10095; Core &#10095; Contracts &#10095; Application &#10095; RestAPIController**. In this class, the individual endpoints are defined via annotation attributes. Access to endpoints can be secured by means of policies.

### Methods

| Parameter | Datentyp | Standardwert | Erforderlich | Beschreibung
| :-------: | -------- | :----------: | :----------: | ------------ 
| 1 | `STRING`<br>`STRING[]` | - | &#10004; | Possible methods are `DELETE`, `GET`, `HEAD`, `PATCH`, `POST` and `PUT`.
| 2 | `STRING` | - | &#10004; | Route: A valid URI.
| 3 | `STRING` | - | &#10004; | Unique name in domain notation.
| 4 | `INTEGER` | 1 | &#10008; | The API version.
<div class="text-align-right">Legend: &#10004; Yes &#10008; No</div>

~~~php
<?php

class BookRestAPI extends RestAPIController
{
    #[API('GET', '/books', 'book.list')]
    public function listBooks(): JsonResponse
    {
        ...
    }
    
    #[API('GET', '/books/{id}', 'book.get')]
    public function getBook(string $bookId): JsonResponse
    {
        ...
    }
    
    #[API('POST', '/books', 'book.create')]
    public function createBook(): JsonResponse
    {
        ...
    }
    
    #[API('DELETE', '/books/{id}', 'book.delete')]
    public function deleteBook(string $bookId): JsonResponse
    {
        ...
    }
}
~~~

### Return value

The return value of an endpoint must always be of the data type **AppsDock &#10095; Core &#10095; Http &#10095; JsonResponse**.

To create a general response, the method **createResponse** can be used.

~~~php
<?php

$this->createResponse(
    int $statusCode = 200,
    array $data = [],
    array $headers = []
);
~~~

If an HTTP status code is to be returned, the method **createStatusResponse** can be used.

~~~php
<?php

$this->createStatusResponse(
    int $statusCode,
    string $message = null,
    array $headers = []
);
~~~

If data is to be returned, the method **createDataResponse** can be used.

~~~php
<?php

$this->createDataResponse(
    ReadModel|ReadModelCollection|null $data,
    int $statusCode = 200,
    array $headers = []
);
~~~

*[API]: Application Programming Interface
*[REST]: Representational State Transfer
*[URI]: Uniform Resource Identifier
