# Sistema de Autenticación con JWT en Spring Boot

## Descripción
Este proyecto implementa un sistema de autenticación y autorización de usuarios utilizando Spring Boot y JSON Web Tokens (JWT). Permite a los usuarios registrarse, iniciar sesión y acceder a recursos protegidos de la aplicación.

## Tecnologías Utilizadas
* **Spring Boot:** Framework Java para crear aplicaciones independientes.
* **Spring Security:** Framework de seguridad para aplicaciones Spring.
* **JWT:** JSON Web Tokens para autenticación sin estado.
* **Base de datos:** (MySQL)
* **Build tool:** (Maven)

## Funcionalidades
* **Registro de usuarios:** Permite a los usuarios crear una nueva cuenta.
* **Inicio de sesión:** Autentica a los usuarios y genera un token JWT.
* **Protección de rutas:** Solo los usuarios autenticados pueden acceder a ciertas rutas.
* **Roles y permisos:** Define roles y permisos para usuarios y controla el acceso a recursos.
* **Refresco de tokens:** Permite a los usuarios renovar sus tokens JWT.

## Configuración
1. **Base de datos:** Configura la conexión a la base de datos en el archivo `application.properties`.
2. **JWT:** Configura las claves y la duración de los tokens en `application.properties`.
3. **Spring Security:** Configura Spring Security para utilizar JWT y proteger las rutas.

## Ejecución
1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/diegolopez-dev/login-jwt.git
2. **Construir el proyecto**
* **mvn clean package**
* **java -jar target/auth-service.jar**

# Ejemplo de solicitud
curl -X POST http://localhost:8080/auth/login \
  -H 'Content-Type: application/json' \
  -d '{"username":"user","password":"password"}'
