### 2. Configuración de Java
1.  Importa el proyecto en tu IDE preferido.
2.  Añade el **MySQL Connector/J** a las librerías del proyecto.
3.  Modifica las credenciales en la clase `ConexionBD.java`:
    ```java
    String URL = "jdbc:mysql://localhost:3306/biblioteca_db";
    String USER = "tu_usuario";
    String PASS = "tu_contraseña";
    ```

---

## 📂 Estructura del Código
*   `Libro.java`: Modelo que define la entidad y sus atributos.
*   `ConexionBD.java`: Gestión del Driver y establecimiento del enlace con MySQL.
*   `LibroDAO.java`: Capa de persistencia donde reside la lógica SQL.
*   `Main.java`: Interfaz de usuario y flujo del programa.

---
*Desarrollado como parte de la formación en Acceso a Datos y Programación JavaEsta es una versión de **README.md** diseñada para destacar en GitHub. Incluye una estructura profesional, iconos (badges) y secciones claras de código y uso que demuestran la calidad de tu trabajo.

---

# 📚 Sistema de Gestión de Biblioteca (JDBC & MySQL)

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-00000F?style=for-the-badge&logo=mysql&logoColor=white)
![JDBC](https://img.shields.io/badge/JDBC-Connector-blue?style=for-the-badge)

Aplicación robusta de consola desarrollada en **Java** para la administración de inventarios bibliográficos. Este proyecto implementa una arquitectura de acceso a datos mediante el patrón **DAO (Data Access Object)** y asegura la integridad de la información mediante **MySQL**.

## 🎯 Objetivo del Proyecto
El propósito de este ejercicio es aplicar conocimientos avanzados de **JDBC** (Java Database Connectivity), gestionando el ciclo de vida completo de un registro (CRUD) y garantizando la seguridad mediante el uso de consultas parametrizadas.

---

## 🚀 Funcionalidades Principales

El sistema ofrece un menú interactivo con las siguientes capacidades:

*   **➕ Registro de Libros:** Alta de nuevos ejemplares incluyendo título, autor, género y precio.
*   **📋 Inventario Completo:** Listado formateado de todos los libros en la base de datos.
*   **🔍 Búsqueda por Autor:** Localización inteligente de títulos mediante coincidencias parciales.
*   **💰 Actualización de Precios:** Modificación precisa de valores monetarios mediante el ID único.
*   **🗑️ Gestión de Bajas:** Eliminación definitiva de registros específicos.

---

## 🛠️ Stack Tecnológico y Conceptos
*   **Lenguaje:** Java (POO avanzada).
*   **Base de Datos:** MySQL (Motor relacional).
*   **Seguridad:** Implementación de `PreparedStatement` para prevenir **SQL Injection**.
*   **Arquitectura:** Separación de responsabilidades en 4 capas (Modelo, DAO, Conexión y Main).

---

## 📋 Configuración del Entorno

### 1. Preparación de la Base de Datos
Ejecuta el siguiente script en tu servidor MySQL para inicializar el esquema:
```sql
CREATE DATABASE biblioteca_db;
USE biblioteca_db;

CREATE TABLE libros (
    id INT AUTO_INCREMENT PRIMARY KEY,
    titulo VARCHAR(100) NOT NULL,
    autor VARCHAR(100) NOT NULL,
    genero VARCHAR(50),
    precio DECIMAL(6,2),
    disponible BOOLEAN
);

-- Datos de prueba
INSERT INTO libros (titulo, autor, genero, precio, disponible) VALUES 
('El Quijote', 'Miguel de Cervantes', 'Novela', 15.50, true),
('1984', 'George Orwell', 'Ciencia ficción', 12.75, false);


2. Configuración de Java
Importa el proyecto en tu IDE preferido.

Añade el MySQL Connector/J a las librerías del proyecto.

Modifica las credenciales en la clase ConexionBD.java:

Java
String URL = "jdbc:mysql://localhost:3306/biblioteca_db";
String USER = "tu_usuario";
String PASS = "tu_contraseña";
📂 Estructura del Código
Libro.java: Modelo que define la entidad y sus atributos.

ConexionBD.java: Gestión del Driver y establecimiento del enlace con MySQL.

LibroDAO.java: Capa de persistencia donde reside la lógica SQL.

Main.java: Interfaz de usuario y flujo del programa.
