# Getting Things Done en Flask

En el archivo [app/flask-app.py](app/flask-app.py) se encuentra una aplicación simplificada que modela el proceso *Getting Things Done* bajo un esquema API REST.

* Diapositivas asociadas a este repositorio se encuentran [aquí](https://docs.google.com/presentation/d/13in0zrKxB3gU6OPA0-G6l0C9trTVvGhtrMD5yUUMPgs/edit?usp=sharing).

* Una lista de reproducción describiendo esta aplicación se encuentra [aquí](https://www.youtube.com/playlist?list=PLphfbydEnqDZPQpLqeW4J0IG4DgVQBKoA).

## Notas


### Acceso a los servicios ofrecidos por el "API" desde el CLI

- Validar si el servicio está arriba:

```
curl -i http://localhost:5000
```

- Consultar por las tareas pendientes:

```
curl -i http://localhost:5000/todo/api/v1.0/tasks
```

- Consultar por una tarea en particular:

```
curl -i http://localhost:5000/todo/api/v1.0/tasks/1
```

- Crear una nueva tarea:

```
curl -i -H "Content-Type: application/json" -X POST -d '{"title": "read a book"}' http://localhost:5000/todo/api/v1.0/tasks
```

- Modificar una tarea existente:

```
curl -i -H "Content-Type: application/json" -X PUT -d '{"done": true}' http://localhost:5000/todo/api/v1.0/tasks/2
```

### Gestión de contenedores

- Para detener la ejecución de los contenedores con borrado de los mismos

```
docker-compose down --rmi all
```

- Para forzar la construcción de la imagen que se usa en la aplicación sin considerar lo que está en *cache*

```
docker-compose build --no-cache --no-rm
```
