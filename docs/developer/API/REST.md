# REST API

## Endpunkte

Um für eine App eigene REST API Endpunkte zu erstellen, legt man eine Klasse an, welche vom *RestAPIController* erbt. In dieser werden über Annotation Attribute die einzelnen Endpunkte definiert.

~~~php
class AppRestAPI extends RestAPIController
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
