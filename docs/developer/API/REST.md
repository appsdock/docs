# REST API

## Endpunkte

Um für eine App eigene REST API Endpunkte zu erstellen, legt man eine Klasse an, welche vom *RestAPIController* erbt. In dieser werden über Annotation Attribute die einzelnen Endpunkte definiert.

~~~php
class AppRestAPI extends RestAPIController
{
    #[API('POST', '/app:create/{id}', 'app.create')]
    public function create(string $appId): JsonResponse
    {
        ...
    }
}
~~~

| Parameter | Datentyp | Standardwert | Erforderlich | Beschreibung
| :-------: | -------- | :----------: | :----------: | ------------ 
| 1 | String\|String[] | - | &#10004; | Methode(n) (DELETE, GET, HEAD, PATCH, POST, PUT)
| 2 | String | - | &#10004; | Route
| 3 | String | - | &#10004; | Eindeutiger Name in Domain-Schreibweise.
| 4 | Integer | 1 | &#10008; | API-Version

| &#10004; Ja | &#10008; Nein
| ----------- | -------------
