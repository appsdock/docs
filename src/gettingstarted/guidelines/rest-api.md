# REST API

AppsDock OS provides a REST API service for external communication.
The service can be used to query as well as manipulate the state of resources.

An overview of all available REST API endpoints can be found [here](../../../api/rest).

## Create an endpoint

The endpoints are defined via annotation attributes, and the access can be secured by policies.

Create a class that inherits from the **AppsDock &#10095; Core &#10095; Contracts &#10095; App &#10095; Application &#10095; RestAPIController**.

~~~php
<?php

use AppsDock\Core\Contracts\App\Application\RestAPIController;
use AppsDock\Core\Http\JsonResponse;
use const AppsDock\API\REST\Book\BOOK_CREATE;
use const AppsDock\API\REST\Book\BOOK_DELETE;
use const AppsDock\API\REST\Book\BOOK_GET;
use const AppsDock\API\REST\Book\BOOK_LIST;

class BookRestAPI extends RestAPIController
{
    #[API('GET', '/books', BOOK_LIST)]
    public function listBooks(): JsonResponse
    {
        ...
    }
    
    #[API('GET', '/books/{id}', BOOK_GET)]
    public function getBook(string $bookId): JsonResponse
    {
        ...
    }
    
    #[API('POST', '/books', BOOK_CREATE)]
    public function createBook(): JsonResponse
    {
        ...
    }
    
    #[API('DELETE', '/books/{id}', BOOK_DELETE)]
    public function deleteBook(string $bookId): JsonResponse
    {
        ...
    }
}
~~~

### Method attributes

| Parameter | Type | Default | Required | Description
| --------- | ---- | :-----: | :------: | ----------- 
| Method | `string` \| `string[]` |  | &#10004; | Possible values are `DELETE`, `GET`, `HEAD`, `PATCH`, `POST` and `PUT`.
| Route | `string` |  | &#10004; | An endpoint route.
| Context | `array` |  | &#10004; | An Array constant with more information about this endpoint.
| Version | `int` | 1 | &#10006; | The API version.

### Return value

The return type of any endpoint must be always an instance of **AppsDock &#10095; Core &#10095; Http &#10095; JsonResponse**.
The following methods are provided by AppsDock OS and should be used to return a valid type.

#### General

~~~php
<?php

$this->createResponse(
    int $statusCode = 200,
    array $data = [],
    array $headers = []
);
~~~

#### HTTP status

~~~php
<?php

$this->createStatusResponse(
    int $statusCode,
    string $message = null,
    array $headers = []
);
~~~

#### Data

~~~php
<?php

$this->createDataResponse(
    ReadModel|ReadModelCollection|null $data,
    int $statusCode = 200,
    array $headers = []
);
~~~

*[API]: Application Programming Interface
*[ID]: Identifier
*[OS]: Operating System
*[REST]: Representational State Transfer
*[URI]: Uniform Resource Identifier
