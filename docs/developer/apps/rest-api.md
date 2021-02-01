# REST Api

Jede App verfügt über eigene REST Api endpoints, die unter folgender URL erreichbar sind:

~~~
https://domain.com/api/my.custom.app/v1/
~~~

## Setup

Jeder endpoint muss (unabhängig der Tiefe mit child resources) muss als YML definiert werden.
Diese Definition muss unter folgendem Ordner abgelegt werden:

~~~
appsdock/apps/my.custom.app/setup/rest
~~~

Der name der rest definition Datei ist der selbe wie der URL name dieser resource.

~~~
URL:  api/my.custom.app/v1/customers
PATH: my.custom.app/setup/rest/customers.yml

URL:  api/my.custom.app/v1/products
PATH: my.custom.app/setup/rest/products.yml
~~~

Diese Datei enhält die Definition dieser und aller child resources von diesem endpoint.

~~~
ENDPOINTS api/my.custom.app/v1:

/customers
/customers/58fac2c5-2f37-4c1b-b0f3-1beae1379b89
/customers/58fac2c5-2f37-4c1b-b0f3-1beae1379b89/orders
/customers/58fac2c5-2f37-4c1b-b0f3-1beae1379b89/orders:export

DEFINITION FILE customers.yml:

/customers:
    title: Kunden
    class: Customer.CustomerResource
    allow: GET POST
    param: id

/customers/orders
    title: Bestellungen des Kundens
    class: Customer.OrderResource
    allow: GET
    param: id
    extend:
        export:
            title: Bestellungen Export
            descr: Exportiert alle Bestellungen des Kundens
~~~

Das Attribute *class* ist eine relative Angabe wo die resource Klasse liegt:

~~~
class: Customer.CustomerResource
path: src/Presentation/Rest/Customer/CustomerResource

class: Customer.OrderResource
path: src/Presentation/Rest/Customer/OrderResource

class: Products.ProductResource
path: src/Presentation/Rest/Products/ProductResource

class: CategoryResource
path: src/Presentation/Rest/CategoryResource
~~~