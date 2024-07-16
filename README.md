# Foro API

## Descripción

Este proyecto es una API REST de un foro, desarrollado con Spring Boot. La API permite a los usuarios crear, listar, actualizar y eliminar tópicos en un foro. También incluye autenticación y autorización utilizando JSON Web Tokens (JWT).

## Requisitos

- Java 17
- Maven
- PostgreSQL

## Configuración

1. **Clonar el repositorio:**

    ```bash
    git clone https://github.com/laurisima/ForoTopic.git
    cd foro
    ```

2. **Configurar la base de datos:**

    Asegúrate de tener PostgreSQL instalado y ejecutándose. Luego, crea una base de datos para el proyecto:

    ```sql
    CREATE DATABASE foro;
    ```

3. **Configurar las propiedades de la aplicación:**

    Edita el archivo `src/main/resources/application.properties` para configurar la conexión a la base de datos PostgreSQL:

    ```properties
    spring.datasource.url=jdbc:postgresql://localhost:8080/foro
    spring.datasource.username=tu-usuario
    spring.datasource.password=tu-contraseña

    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect

    spring.security.jwt.secret-key=tu-secreta-llave
    ```

4. **Construir el proyecto:**

    Ejecuta el siguiente comando para construir el proyecto y descargar las dependencias:

    ```bash
    mvn clean install
    ```

## Ejecución

Para ejecutar la aplicación, utiliza el siguiente comando:

```bash
mvn spring-boot:run
