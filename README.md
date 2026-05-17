# Plataforma Web de Gestión de Tutorías Académicas

| Información Académica | Detalles del Proyecto |
| :--- | :--- |
| **Institución** | Unidades Tecnológicas de Santander (UTS) |
| **Asignatura** | Java (B192) |
| **Proyecto** | Sistema de Gestión de Tutorías |
| **Desarrolladores** | Maria Fernanda Cáceres Ortiz<br>Keyner Camilo Bueno Mendoza<br>Juan Felipe Celis Carreño|

---

## Descripción del Proyecto
Este sistema es una solución web integral diseñada para optimizar, automatizar y estructurar el proceso de agendamiento y control de tutorías académicas. La plataforma actúa como un puente directo entre estudiantes y docentes, eliminando las barreras de comunicación tradicionales y garantizando un uso eficiente del tiempo de asesoría.

El sistema mitiga problemáticas comunes como el cruce de horarios, la falta de visibilidad de la disponibilidad docente y la ausencia de un registro histórico centralizado de las asistencias.

---

## Entorno de Trabajo y Stack Tecnológico

| Componente | Tecnología Seleccionada | Descripción Técnica |
| :--- | :--- | :--- |
| **Lenguaje** | Java 17 | Uso de estructuras modernas (Records) y rendimiento LTS. |
| **Backend** | Spring Boot 3.x | Arquitectura desacoplada basada en el patrón MVC. |
| **Seguridad** | Spring Security | Control de acceso por roles (RBAC) y cifrado BCrypt. |
| **Vistas** | Thymeleaf + Bootstrap | Renderizado dinámico en servidor con diseño responsivo. |
| **Persistencia** | Spring Data JPA | Mapeo objeto-relacional optimizado mediante Hibernate. |
| **Base de Datos** | MariaDB | Motor relacional para consistencia y control de concurrencia. |
| **Gestor** | Maven | Administración centralizada de dependencias y ciclo de vida. |

---

## Arquitectura del Sistema (Módulos Principales)

El sistema segmenta sus capacidades funcionales a través de tres perfiles de usuario claramente definidos:

### 1. Módulo Administrativo
* **Gestión de Identidades:** Alta, modificación e inhabilitación de cuentas de usuarios (Docentes y Estudiantes).
* **Control del Catálogo:** Administración centralizada de las asignaturas académicas y dependencias departamentales.

### 2. Módulo del Docente
* **Oferta Horaria:** Registro dinámico de franjas de disponibilidad de tiempo vinculadas a asignaturas específicas.
* **Control de Aula:** Gestión de estados de citas (Pendiente, Realizada, Cancelada) y validación de asistencia estudiantil con registro de observaciones.

### 3. Módulo del Estudiante
* **Motor de Búsqueda:** Filtros avanzados por nombre de docente, áreas académicas o asignaturas particulares.
* **Agendamiento Autónomo:** Reserva inmediata de cupos disponibles en tiempo real, previniendo conflictos de concurrencia.

---

## Atributos de Calidad (Requerimientos No Funcionales)

* **Seguridad Estricta:** Acceso protegido a rutas URL mediante contextos de Spring Security según el rol asignado (`ROLE_ADMIN`, `ROLE_DOCENTE`, `ROLE_ESTUDIANTE`).
* **Diseño Adaptable:** Interfaz de usuario responsiva construida con Bootstrap, garantizando usabilidad tanto en navegadores de escritorio como en dispositivos móviles.
* **Consistencia Relacional:** El motor MariaDB asegura que no existan colisiones de reservas simultáneas para un mismo bloque horario.

---
