# ebac-backend-java

![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-NoSQL-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Spring](https://img.shields.io/badge/Spring-IoC-6DB33F?style=for-the-badge&logo=spring&logoColor=white)

> Este repositorio es un **fork** del material de referencia del curso de Backend Java de EBAC, creado por [spcruzaley](https://github.com/spcruzaley/ebac-backend-java). Lo conservo como guía de estudio; mis propias implementaciones de cada módulo están en los repositorios enlazados más abajo.

## Descripción

Código de ejemplo organizado por módulo del curso. Cada paquete contiene una clase `Contexto` ejecutable y, en algunos casos, una carpeta `recursos` con notas y comandos de apoyo.

| Módulo | Tema |
| --- | --- |
| `modulo33` | Conexión a MySQL con JDBC y consultas con `Statement` (incluye notas de Docker, DDL y DML) |
| `modulo34` | Patrón DTO + Model y CRUD con `PreparedStatement` e interfaz genérica `OperacionesCRUD<T>` |
| `modulo35` | Persistencia con JPA / Hibernate y `persistence.xml` |
| `modulo36` | CRUD con MongoDB usando el driver síncrono |
| `modulo37` | Inyección de dependencias con Spring por XML (setter, constructor y anotaciones) |
| `modulo38` | Configuración por anotaciones: `@Configuration`, `@Bean`, `@Value`, `@Qualifier` |

## Mis implementaciones relacionadas

| Tema | Repositorio |
| --- | --- |
| JDBC y CRUD con MySQL | [TelcelUsuarios](https://github.com/Donaldo500/TelcelUsuarios), [telcelusers](https://github.com/Donaldo500/telcelusers) |
| JPA y MongoDB | [backend-java](https://github.com/Donaldo500/backend-java) |
| Spring IoC e inyección de dependencias | [modulo61](https://github.com/Donaldo500/modulo61) |

## Tecnologías utilizadas

- Java, Maven
- JDBC, MySQL Connector/J
- JPA / Hibernate
- MongoDB Java Driver
- Spring Framework

## Instalación y uso

1. Levanta los servicios necesarios (según `modulo33/recursos/notes.txt`):

   ```bash
   docker run --rm --name mysql -e MYSQL_ROOT_PASSWORD=root -d -p 3306:3306 mysql
   docker run --rm --name adminer -d -p 8080:8080 adminer
   ```

2. Crea las tablas indicadas en las notas de cada módulo.

3. Ejecuta el módulo que quieras revisar:

   ```bash
   git clone https://github.com/Donaldo500/ebac-backend-java.git
   cd ebac-backend-java
   mvn compile exec:java -Dexec.mainClass="com.ebac.modulo34.Contexto"
   ```

## Créditos

Contenido original de [spcruzaley/ebac-backend-java](https://github.com/spcruzaley/ebac-backend-java). Las contribuciones al material deben dirigirse al repositorio original.
