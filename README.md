# 🚀 Desafíos Técnicos: Estructuras y Registros en Java

Este apartado contiene una ruta de aprendizaje práctica para dominar el uso de **Classes** (POJOs) y **Records** en Java.

---

## 📊 Tabla de Contenidos
| Nivel | Enfoque Técnico | Icono |
| :--- | :--- | :--- |
| **Principiante** | Fundamentos e Inmutabilidad | 🟢 |
| **Intermedio** | Lógica, Validaciones y Streams | 🟡 |
| **Avanzado** | Arquitectura, Composición y DTOs | 🔴 |

---

## 🟢 Nivel Principiante: Fundamentos
> *Enfocado en entender la sintaxis básica y la diferencia entre datos mutables e inmutables.*

### 📚 Ejercicio 1: El Registro de Libros
*   **Concepto:** Implementar una estructura inmutable para transporte de datos.
*   **Tarea:** 
    1. Crea un `record` llamado `Libro` con los campos: `titulo` (String), `autor` (String) y `precio` (double).
    2. En tu clase `Main`, instancia dos objetos de tipo `Libro`.
    3. Imprime los datos usando `toString()` y accede a un campo usando el método de acceso (ej. `libro.titulo()`).

### 📦 Ejercicio 2: Control de Inventario
*   **Concepto:** Gestionar estado mutable mediante clases tradicionales.
*   **Tarea:** 
    1. Crea una clase `Producto` con atributos `nombre` (String) e `stock` (int).
    2. Implementa un constructor, getters y un método `vender(int cantidad)` que valide si hay existencias antes de restar.

---

## 🟡 Nivel Intermedio: Lógica y Colecciones
> *Uso de lógica de negocio dentro de las estructuras de datos.*

### 🛡️ Ejercicio 3: Validación de Datos (Constructor Compacto)
*   **Concepto:** Integridad de datos en el punto de creación.
*   **Tarea:** 
    1. Crea un `record` `Estudiante` con `nombre`, `matricula` y `calificacion`.
    2. Implementa un **constructor compacto** que lance una `IllegalArgumentException` si la calificación no está entre 0 y 10.
    3. Filtra una lista de estudiantes para mostrar solo los aprobados.

### 💸 Ejercicio 4: Procesamiento de Transacciones con Streams
*   **Concepto:** Manipulación de colecciones de registros de forma funcional.
*   **Tarea:** 
    1. Crea un `record` `Transaccion` con `id`, `monto` y `tipo` ("DEBITO" o "CREDITO").
    2. Usa **Java Streams** para filtrar las de tipo "CREDITO" y calcular la suma total de los montos.

---

## 🔴 Nivel Avanzado: Arquitectura y Patrones
> *Estructuras complejas y separación de responsabilidades.*

### 🛰️ Ejercicio 5: Composición de Registros (Sensores)
*   **Concepto:** Manejo de estructuras anidadas y tipos complejos.
*   **Tarea:** 
    1. Crea registros anidados: `Ubicacion` (lat/long) -> `Lectura` (valor/unidad) -> `Sensor` (id/ubicacion/lista de lecturas).
    2. Implementa una función que calcule el promedio técnico de todas las lecturas de un sensor.

### 🔄 Ejercicio 6: Patrón DTO (Data Transfer Object)
*   **Concepto:** Transformación de entidades de negocio a registros de transporte.
*   **Tarea:** 
    1. Define una clase `UsuarioEntity` con campos sensibles (id, password, email).
    2. Crea un `record` `UsuarioDTO` con solo los datos públicos (`username`, `email`).
    3. Crea un mapper que convierta la entidad en el DTO para proteger la información sensible.

---

## 🛠️ Stack Tecnológico
*   ☕ **Java 17+** (Soporte nativo de Records)
*   🏗️ **Maven/Gradle**
*   🧪 **JUnit 5** (Opcional para testing)
