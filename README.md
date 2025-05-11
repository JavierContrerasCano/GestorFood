# ZGESTOR_ACADEMIA_06

Este repositorio contiene el código fuente del reporte ABAP `ZGESTOR_ACADEMIA_06`, desarrollado en SAP GUI para la gestión de cursos académicos.

---

## 📌 Descripción general

Este reporte proporciona una interfaz para:

1. **Listar cursos existentes** en base a múltiples criterios (DNI, ID de curso, fechas, familia profesional, provincia, etc.).
2. **Insertar nuevos registros de cursos** para alumnos y profesores, incluyendo validaciones previas.

---

## ⚙️ Funcionalidades principales

### 🔹 Listado de cursos
- Permite consultar cursos desde la tabla `ZACADEMIA_06`.
- Usa ALV (ABAP List Viewer) para mostrar los resultados de forma estructurada y clara.

### 🔹 Inserción de cursos
- Verifica si el **profesor** y el **alumno** están registrados.
  - Si no lo están, ofrece navegar a los reportes `ZGESTOR_PROFESOR_06` o `ZGESTOR_ALUMNOS_06`.
- Comprueba si el alumno:
  - Ya está inscrito en el mismo curso.
  - Está en un curso con fechas solapadas.
- Inserta el nuevo curso tras confirmación.

---

## 🧱 Estructuras y tablas Z utilizadas

- `ZACADEMIA_06`: Cursos y su relación con alumnos/profesores.
- `ZALUMNOS_CURSO_6`: Datos de alumnos.
- `ZTAB_PROFESOR_06`: Datos de profesores.
- Tipos y dominios personalizados (`ZED_*`, `Z_DNI*`, etc.) para campos específicos.

---

## 🖥️ Interfaz de usuario

Organizada por bloques en la `SELECTION-SCREEN`:

- Filtros de búsqueda (SELECT-OPTIONS)
- Datos de entrada (PARAMETERS)
- Botones de acción (PUSHBUTTONS)
  - Listar cursos
  - Insertar curso
  - Volver al menú principal

---

## 🚨 Validaciones

- Existencia del profesor y alumno.
- Solapamiento de fechas en cursos.
- Duplicidad de inscripciones.

---

## 📅 Autor y mantenimiento

- Autor: Javier Contreras Cano
- Fecha:ABRIL 2025
- SAP Version

---

## 📜 Licencia

Este proyecto se distribuye con fines educativos y de documentación. No se debe utilizar en entornos productivos sin validación previa del código y autorización correspondiente.
