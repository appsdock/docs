# REST API

## Endpunkte

Um für eine App eigene REST API Endpunkte zu erstellen, legt man eine Klasse an, welche vom ***AppsDock\Core\Contracts\App\Application\RestAPIController*** erbt. In dieser werden über Annotation Attribute die einzelnen Endpunkte definiert. Der Zugriff auf Endpunkte kann mittels Richtlinien abgesichert werden.

### Methoden

~~~php
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

| Parameter | Datentyp | Standardwert | Erforderlich | Beschreibung
| :-------: | -------- | :----------: | :----------: | ------------ 
| 1 | String\|String[] | - | &#10004; | Methoden: DELETE, GET, HEAD, PATCH, POST und PUT.
| 2 | String | - | &#10004; | Route: Valide URL.
| 3 | String | - | &#10004; | Eindeutiger Name in Domain-Schreibweise.
| 4 | Integer | 1 | &#10008; | API-Version.

| &#10004; Ja | &#10008; Nein
| ----------- | -------------

#### Rückgabewerte

Der Rückgabewert eines Endpunkts muss immer vom Datentyp ***AppsDock\Core\Http\JsonResponse*** sein.

Um eine allgemeine Rückmeldung zu erzeugen, kann die Methode ***createResponse*** verwendet werden.

~~~php
$this->createResponse(
    int $statusCode = 200,
    array $data = [],
    array $headers = []
);
~~~

Soll ein HTTP-Status-Code zurückgegeben werden, kann die Methode ***createStatusResponse*** verwendet werden.

~~~php
$this->createStatusResponse(
    int $statusCode,
    string $message = null,
    array $headers = []
);
~~~

Sollen Daten zurückgegeben werden, kann die Methode ***createDataResponse*** verwendet werden.

~~~php
$this->createDataResponse(
    ReadModel|ReadModelCollection|null $data,
    int $statusCode = 200,
    array $headers = []
);
~~~
