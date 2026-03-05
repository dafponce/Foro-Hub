---

# 🚀 ForoHub API

### API REST para la gestión de foros de discusión

ForoHub API es un proyecto backend desarrollado con **Java y Spring Boot** que permite administrar un sistema de foros donde los usuarios pueden crear temas de discusión, responder a otros usuarios y participar en conversaciones relacionadas con distintos cursos.

La API está diseñada siguiendo principios **REST**, incorporando autenticación segura mediante **JWT**, control de acceso por roles y buenas prácticas de desarrollo como validaciones, manejo centralizado de errores y documentación automática.

---

# 📌 Descripción del proyecto

**ForoHub API** funciona como el backend de una plataforma de foros. A través de esta API los usuarios pueden interactuar con distintos tópicos, participar en conversaciones y gestionar contenido dentro del sistema.

Entre sus principales funciones se encuentran:

* 💬 Crear y administrar **tópicos de discusión**
* 💭 Publicar **respuestas dentro de los tópicos**
* 📚 Organizar temas según **cursos**
* 🔐 Autenticarse de forma segura usando **JWT**
* 👥 Control de acceso basado en **roles de usuario**
* 📊 Consultar información usando **paginación y filtros**

Además, el sistema incluye mecanismos para proteger la información, de modo que los usuarios solo puedan modificar o eliminar su propio contenido, mientras que moderadores o administradores cuentan con permisos adicionales.

---

# 📊 Estado del proyecto

🚧 **Proyecto actualmente en desarrollo**

Versión actual:

`v0.0.1-SNAPSHOT`

Muchas funcionalidades principales ya están implementadas, aunque todavía se siguen agregando mejoras y nuevas características.

---

# ⚙️ Funcionalidades principales

Actualmente la API permite:

### 🔐 Autenticación y seguridad

* Registro de nuevos usuarios
* Inicio de sesión con generación de **token JWT**
* Sistema de **roles** (USER, MODERATOR, ADMIN)
* Restricción de acceso a endpoints según permisos

---

### 📝 Gestión de tópicos

Los usuarios pueden:

* Crear nuevos tópicos
* Consultar tópicos existentes
* Editar sus propios tópicos
* Eliminarlos mediante **borrado lógico**

También se implementó un sistema de **estado de tópicos** para indicar si están abiertos o cerrados.

---

### 💭 Sistema de respuestas

Cada tópico puede tener múltiples respuestas. El sistema permite:

* Crear respuestas
* Editar o eliminar respuestas propias
* Marcar una respuesta como **solución**

---

### 📚 Gestión de cursos

Los tópicos están asociados a cursos específicos.
Solo los usuarios con rol **ADMIN** pueden:

* Crear cursos
* Actualizar información de cursos
* Eliminar cursos (borrado lógico)
* Filtrar cursos por categoría

---

### 👤 Gestión de usuarios

La API también incluye operaciones relacionadas con los usuarios:

* Consultar perfil del usuario autenticado
* Actualizar email
* Eliminar cuenta propia
* Desactivar usuarios (solo administradores)

---

# 🛠️ Tecnologías utilizadas

El proyecto fue desarrollado utilizando las siguientes tecnologías:

* **Java 17**
* **Spring Boot**
* **Spring Security**
* **Spring Data JPA**
* **MySQL**
* **Flyway** para migraciones de base de datos
* **JWT** para autenticación
* **Swagger / OpenAPI** para documentación
* **Maven** para gestión de dependencias
* **Lombok** para reducir código repetitivo

---

# 📦 Instalación del proyecto

### 1️⃣ Clonar repositorio

```bash
git clone https://github.com/tu-usuario/forohub-api.git
cd forohub-api
```

### 2️⃣ Crear base de datos

```sql
CREATE DATABASE forohub_api;
```

### 3️⃣ Configurar conexión

Editar el archivo:

```
src/main/resources/application.properties
```

Ejemplo:

```properties
spring.datasource.url=jdbc:mysql://localhost/forohub_api
spring.datasource.username=tu_usuario
spring.datasource.password=tu_password
```

---

### 4️⃣ Ejecutar el proyecto

```bash
mvn spring-boot:run
```

La aplicación quedará disponible en:

```
http://localhost:8080
```

---

# 📖 Documentación de la API

Una vez ejecutada la aplicación se puede acceder a la documentación interactiva mediante **Swagger** en:

```
http://localhost:8080/swagger-ui/index.html
```

Desde ahí es posible:

* ver los endpoints disponibles
* probar peticiones
* revisar los modelos de datos
* consultar los códigos de respuesta

---

# 👨‍💻 Autor

**Daniel Flores**

Proyecto realizado como práctica para el aprendizaje de **Spring Boot, desarrollo de APIs REST y seguridad con JWT**.

---





