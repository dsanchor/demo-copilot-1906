# API de Usuarios

La API de Usuarios permite realizar operaciones CRUD sobre un recurso de usuario. A continuación, se detallan los endpoints disponibles y ejemplos de cómo interactuar con ellos mediante `curl`.

## Endpoints

### Obtener todos los usuarios

- **GET** `/users`

#### Ejemplo de `curl`:

```bash
curl -X GET http://localhost:8080/users
```

### Obtener un usuario por ID

- **GET** `/users/{userId}`

#### Ejemplo de `curl`:

```bash
curl -X GET http://localhost:8080/users/1
```

### Crear un nuevo usuario

- **POST** `/users`

#### Ejemplo de `curl`:

```bash
curl -X POST http://localhost:8080/users \
     -H 'Content-Type: application/json' \
     -d '{"id": "1", "nombre": "Juan", "apellido": "Pérez", "email": "juan.perez@example.com"}'
```

### Actualizar un usuario

- **PUT** `/users/{userId}`

#### Ejemplo de `curl`:

```bash
curl -X PUT http://localhost:8080/users/1 \
     -H 'Content-Type: application/json' \
     -d '{"nombre": "Juan actualizado", "apellido": "Pérez", "email": "juan.perez@example.com"}'
```

### Eliminar un usuario

- **DELETE** `/users/{userId}`

#### Ejemplo de `curl`:

```bash
curl -X DELETE http://localhost:8080/users/1
```

## Containerización

Para construir la imagen de Docker, ejecutar el siguiente comando:

```bash
docker build -t users-api .
```

Para ejecutar la imagen de Docker, ejecutar el siguiente comando:

```bash
docker run -p 8080:8080 users-api
```
