# Desafíos Técnicos: Estructuras y Registros en Java

Este apartado contiene ejercicios prácticos para dominar el uso de **Classes** (POJOs) y **Records** en Java, abarcando desde la gestión básica de datos hasta arquitecturas avanzadas.

---

## 🟢 Nivel Principiante (Fundamentos)

### Ejercicio 1: El Registro de Libros
**Objetivo:** Implementar una estructura inmutable para transporte de datos.
- Crea un `record` llamado `Libro` con los campos: `titulo` (String), `autor` (String) y `precio` (double).
- En tu clase `Main`, instancia dos objetos de tipo `Libro`.
- Imprime los datos en la consola usando el método `toString()` y accede a un campo específico usando el método de acceso (ej. `libro.titulo()`).

### Ejercicio 2: Control de Inventario
**Objetivo:** Gestionar estado mutable mediante clases tradicionales.
- Crea una clase `Producto` con atributos `nombre` (String) y `stock` (int).
- Implementa un constructor, métodos `getter` y un método `setter` para actualizar el stock.
- Añade un método `vender(int cantidad)` que valide si hay suficiente stock antes de restar.

---

## 🟡 Nivel Intermedio (Lógica y Colecciones)

### Ejercicio 3: Validación de Datos en Records
**Objetivo:** Uso de constructores compactos para integridad de datos.
- Crea un `record` llamado `Estudiante` con `nombre`, `matricula` y `calificacion`.
- Implementa un **constructor compacto** que lance una `IllegalArgumentException` si la calificación no está entre 0 y 10.
- Crea una lista (`ArrayList`) de estudiantes y filtra a los aprobados.

### Ejercicio 4: Procesamiento de Transacciones con Streams
**Objetivo:** Manipulación de colecciones de registros.
- Crea un `record` `Transaccion` con `id`, `monto` y `tipo` (String: "DEBITO" o "CREDITO").
- Crea una lista de 5 transacciones.
- Utiliza el API de **Streams** para filtrar solo las de tipo "CREDITO" y sumar el monto total.

---

## 🔴 Nivel Avanzado (Arquitectura y Patrones)

### Ejercicio 5: Composición de Registros (Sensores)
**Objetivo:** Manejo de estructuras anidadas y tipos complejos.
- Crea un `record` `Ubicacion` (latitud, longitud).
- Crea un `record` `Lectura` (valor, unidad, marcaDeTiempo).
- Crea un `record` `Sensor` que contenga un `id`, una `Ubicacion` y una `List<Lectura>`.
- Implementa una función que reciba un `Sensor` y calcule el promedio de sus lecturas técnicas.

### Ejercicio 6: Patrón DTO (Data Transfer Object)
**Objetivo:** Transformación de entidades de negocio a registros de transporte.
- Define una clase `UsuarioEntity` con campos sensibles (id, username, password, email, ultimaConexion).
- Crea un `record` `UsuarioDTO` que solo contenga `username` y `email`.
- Crea una clase de servicio con un método `toDTO(UsuarioEntity entity)` que realice la conversión. Esto simula el envío de datos a una API protegiendo información sensible.

---

## 🛠️ Tecnologías Sugeridas
- Java 17 o superior (para soporte completo de `records`).
- Maven o Gradle para gestión de dependencias.
- JUnit 5 si deseas añadir pruebas unitarias a tus soluciones.
