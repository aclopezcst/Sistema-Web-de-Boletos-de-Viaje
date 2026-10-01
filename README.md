# Plataforma de venta y procesamiento de boletos de viaje 
Plataforma web dinámica orientada al sector transporte para la consulta, selección y compra de pasajes de autobús. Integra procesamiento simulado de métodos de pago (tarjetas VISA y PayPal) y un diseño para la gestión transaccional de usuarios y pasajes
¡Bienvenido a **Senda Express**! Este repositorio contiene una solución web full-stack diseñada para la consulta de rutas, selección de viajes y procesamiento seguro de pagos con integración simulada de **PayPal** y pasarela de tarjetas **VISA**.

Este sistema no es solo una interfaz de usuario; integra validaciones del lado del servidor, controladores PHP para procesamiento de transacciones y un esquema estructurado de base de datos SQL para asegurar la persistencia transaccional.

* **Frontend:**
  * `PaginaInicial.html` & `Compra.html`: Modulos de navegación e interfaz principal de usuario.
  * `diseño.css` & `diseño1.css`: Archivos de hojas de estilo adaptadas para una experiencia responsive.
  * `form_Visa.html` & `PAYPAL.html`: Formularios dinámicos para captura de credenciales financieras.
* **Backend (PHP):**
  * `getconex.php`: Módulo centralizado de conexión segura a la base de datos MySQL/SQL Server[cite: 1].
  * `Procesar_pago.php` & `proceso_pago_VISA.php`: Script encargado de procesar y tokenizar la transacción[cite: 1].
  * `MetodoPaypal.php`: Lógica de redirección e integración para cobros con cuenta PayPal[cite: 1].
* **Base de Datos (SQL):**
  * `SQLQueryGpoSenda.sql`: Script de creación del esquema principal[cite: 1].
  * `Tabla_Compra.sql`, `tabla pagosVISA.sql` y `Tabla de Paypal.sql`: Definición de tablas y constraints para garantizar la integridad referencial[cite: 1].

 **Instrucciones de Despliegue y Uso**

Sigue estos pasos para desplegar el entorno de desarrollo e interactuar con la plataforma:

### 1. Requisitos Previos
* Servidor Web Local (XAMPP, WAMP o Laragon) con soporte para **PHP 7.4+** y **MySQL**.
* Navegador web moderno (Chrome, Edge, Firefox).

### 2. Configuración de la Base de Datos
1. Inicia tus servicios de Apache y MySQL en XAMPP.
2. Accede a `phpMyAdmin` (o tu gestor de BD de preferencia).
3. Crea una nueva base de datos llamada `gpo_senda`.
4. Importa secuencialmente los siguientes archivos ubicados en la raíz del proyecto:
   * `SQLQueryGpoSenda.sql`[cite: 1]
   * `Tabla_Compra.sql`[cite: 1]
   * `tabla pagosVISA.sql`[cite: 1]
   * `Tabla de Paypal.sql`[cite: 1]

### 3. Configuración del Servidor Web
1. Clona este repositorio dentro de la carpeta pública de tu servidor local (`htdocs` en XAMPP):
   ```bash
   git clone [https://github.com/tu-usuario/senda-express-pia.git](https://github.com/tu-usuario/senda-express-pia.git)
