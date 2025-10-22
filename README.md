# Proyecto 3: Análisis de Logs y Pruebas de Bases de Datos (App Taxis)

Este proyecto demuestra habilidades técnicas avanzadas en la investigación de errores (troubleshooting), yendo más allá de la interfaz para encontrar la causa raíz (root cause) mediante el análisis de logs de servidor y la ejecución de consultas SQL complejas.

---

### 1. Objetivo del Proyecto

El objetivo era investigar dos problemas reportados en una aplicación de taxis:
1.  **Investigación de Logs:** Identificar solicitudes sospechosas desde una IP específica y aislar errores 400/500 en los logs del servidor.
2.  **Validación de Datos (SQL):** Investigar quejas de clientes sobre la falta de taxis y discrepancias en los costos de los viajes, consultando directamente la base de datos PostgreSQL.

---

### 2. Mi Rol y Responsabilidades

* **Análisis de Logs (Consola):** Me conecté a un servidor remoto (Linux) para analizar archivos de log. Usé comandos de consola (**grep**) para filtrar millones de líneas y aislar las solicitudes relevantes por IP y código de error (400, 500).
* **Análisis de Datos (SQL):** Escribí consultas **SQL avanzadas** para validar hipótesis de negocio. Esto incluyó el uso de `GROUP BY` y `HAVING` para encontrar compañías con pocos autos, y el uso de `CASE` para segmentar datos (ej. condiciones climáticas).
* **Análisis de Causa Raíz:** Conecté los hallazgos de la base de datos con los problemas reportados para proporcionar al equipo de desarrollo una causa raíz clara.

---

### 3. Evidencias y Resultados

#### A. Análisis de Logs en Consola (Linux)
Filtré los logs del servidor para encontrar errores 400 y 500 en un día específico y los exporté a archivos separados para un análisis más profundo.

<img width="1067" height="455" alt="Captura de pantalla 2025-10-21 a la(s) 7 45 24 p m" src="https://github.com/user-attachments/assets/7c229723-759b-4920-a187-7afb8d80e47e" />

#### B. Consultas SQL Avanzadas (PostgreSQL)
Escribí consultas complejas para responder preguntas de negocio. La siguiente consulta usa `JOIN`, `GROUP BY` y `HAVING` para encontrar compañías de taxis con menos de 100 vehículos, confirmando la queja de los usuarios.

<img width="896" height="527" alt="Captura de pantalla 2025-10-21 a la(s) 8 51 37 p m" src="https://github.com/user-attachments/assets/69ab519b-4ba8-4172-96a3-6d42aa47eaeb" />


#### C. Resultados de la Validación de Datos
La consulta confirmó la hipótesis: varias compañías tenían un número insuficiente de vehículos. La siguiente tabla es el resultado de la consulta.

<img width="940" height="567" alt="Captura de pantalla 2025-10-21 a la(s) 8 57 32 p m" src="https://github.com/user-attachments/assets/ac9a3db9-706c-49cb-8e3f-75b8c426bbd8" />

---

### 4. Tecnologías y Herramientas Utilizadas

* **Base de Datos:** PostgreSQL
* **Consola:** Consola de Comandos (Linux/Bash), `grep`
* **Habilidades:** SQL Avanzado (GROUP BY, HAVING, CASE, JOINs), Análisis de Logs (Log Analysis), Análisis de Causa Raíz (RCA), Pruebas de Bases de Datos.
