# OpenAPI
Estándar o conjunto de reglas que define como describir, visaulizar y crear API's

Open API necesita un software para funcionar, ese software es Swagger, FastAPI utiliza Swagger UI, que permite mostrar la API documentada.
Otra alternativa es ReDoc.

FastAPI -> Swagger -> OpenAPI

## Acceder a Swagger UI
`localhost/docs`

OAS -> OpenAPI Specification

## Acceder a ReDoc
`localhost/redoc`


## Diccionario

#Path Operations 
* Paths : Son direcciones que van después del nombre del domino, ejemplo:

```
myapi.com  /  tweets
  domain       path
```
* Operation: Método HTTP

```
-GET: traer información
-POST: enviar información
-PUT: actualizar información
-DELETE: borrar información
-OPTIONS: devolver un header adicional llamado allow, que contiene los métodos HTTP que se pueden utilizar en ese endpoint
-HEAD: devolver información del documento pero no el documento en sí
-PATH: hacer actualizaciones parciales porque PUT cambia todo el contenido
-TRACE: observa la petición, un debugging
```

> Path Operation: Dirigirse a una ruta con un método HTTP

```python
path operation decorator: @app.get("/")
path operation function:  def home():
                              return {"hello" : "world"}
```

* Path parameter: Una variable definida dentro de un path, por lo general se utilizan para señalar un recurso específico dentro de una colección, su paso es **obligatorio**

`localhost/users/{username}`

* Query parameters: Van después de un signo de interrogación `?`, con un nombre y valor y separados por `&`, los query params son opcionales.

`localhost/user/details?age=20&height=180`

* Request body: Es el body de una petición HTTP, se envía con JSON

* Response body: Es cuando el servidor responde a la petición, se envía con JSON

