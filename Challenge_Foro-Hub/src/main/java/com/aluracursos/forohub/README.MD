# API de Foro - Backend

Este proyecto es una API REST desarrollada con Java y Spring Boot que permite gestionar un sistema básico de foro donde los usuarios pueden crear y administrar tópicos de discusión.

La aplicación sigue una arquitectura basada en controladores, servicios y repositorios, permitiendo una estructura organizada para el desarrollo backend.

---

# Tecnologías utilizadas

- Java 17
- Spring Boot
- Spring Data JPA
- Spring Security
- PostgreSQL
- Maven
- API REST

---

# Estructura del proyecto

```
src/main/java/com/foro/api

AplicacionForo

controladores
├── ControladorTopico.java
└── ControladorAuth.java

modelos
├── Usuario.java
└── Topico.java

repositorios
├── RepositorioUsuario.java
└── RepositorioTopico.java

servicios
├── ServicioUsuario.java
└── ServicioTopico.java

configuracion
└── ConfiguracionCors.java
```

---

# Configuración del proyecto

## 1. Clonar el repositorio

```bash
git clone https://github.com/TU_USUARIO/foro-api-backend.git
```

---

## 2. Crear la base de datos

En PostgreSQL crear la base de datos:

```sql
CREATE DATABASE foro_db;
```

---

## 3. Configurar la conexión

Editar el archivo:

```
src/main/resources/application.properties
```

Configuración:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/foro_db
spring.datasource.username=postgres
spring.datasource.password=1234

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

server.port=8080
```

---

# Ejecutar el proyecto

Desde tu IDE ejecuta la clase principal:

```
AplicacionForo.java
```

La aplicación iniciará en:

```
http://localhost:8080
```

---

# Endpoints de la API

## Registrar usuario

POST

```
/auth/registro
```

Body JSON:

```json
{
  "nombre": "Andres",
  "correo": "andres@email.com",
  "contrasena": "123456"
}
```

---

## Crear tópico

POST

```
/api/topicos
```

Body JSON:

```json
{
  "titulo": "Problema con Spring",
  "mensaje": "No entiendo JPA"
}
```

---

## Listar tópicos

GET

```
/api/topicos
```

---

## Eliminar tópico

DELETE

```
/api/topicos/{id}
```

---

# Pruebas de la API

La API puede probarse utilizando herramientas como Postman o Insomnia.

---

# Autor

Proyecto desarrollado como práctica de desarrollo backend con Spring Boot para la construcción de APIs REST.

---

# Licencia

Este proyecto es de uso educativo y libre para fines de aprendizaje.