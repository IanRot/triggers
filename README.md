# Documentación Completa sobre Triggers

## 1. ¿Qué es un Trigger?

Un Trigger (o Disparador) es un bloque de código que se ejecuta automáticamente en respuesta a ciertos eventos en una base de datos, como operaciones de inserción (INSERT), actualización (UPDATE) o eliminación (DELETE).

Está asociado a una tabla o vista y permite aplicar reglas de negocio directamente en el motor de base de datos.

## 2. ¿Para qué sirve un Trigger?

Un trigger sirve para:

Automatizar tareas repetitivas.

Validar o auditar datos antes/después de un cambio.

Aplicar reglas de negocio complejas.

Registrar cambios en bitácoras o historiales.

Mantener integridad entre tablas relacionadas.

## 3. ¿Cuándo se puede usar un Trigger?

Los triggers se usan comúnmente en escenarios como:

Auditar cambios de datos (log de auditoría).

Validar datos antes de insertar/actualizar.

Actualizar automáticamente otra tabla relacionada.

Restringir operaciones no deseadas.

## 4. Estructura de un Trigger

![image](https://github.com/user-attachments/assets/e1299dc0-633f-4784-8b9a-a4f086acca65)


#### Componentes:

BEFORE: se ejecuta antes de que ocurra el evento.

AFTER: se ejecuta después de que ocurra el evento.

INSTEAD OF: reemplaza el evento (común en vistas).

FOR EACH ROW: se ejecuta para cada fila afectada.

## 5. Tipos de Trigger

BEFORE INSERT

AFTER INSERT

BEFORE UPDATE

AFTER UPDATE

BEFORE DELETE

AFTER DELETE

INSTEAD OF (en vistas, principalmente)

## 6. ¿Cuándo ejecuta su acción un Trigger?

Un trigger ejecuta su acción:

Inmediatamente antes o después del evento definido (según el tipo).

Por cada fila afectada si está definido como FOR EACH ROW.

## 7. Ejemplo de un Trigger
![image](https://github.com/user-attachments/assets/2c9e3524-d4cf-4bfd-aa23-e5771bf46684)

Este trigger guarda una entrada en la tabla auditoria cada vez que se inserta un registro en empleados.

## 8. Trigger Marketing

En marketing, un "trigger" puede referirse a un evento automatizado que desencadena una acción, como:

Enviar un correo de bienvenida al registrarse.

Activar un cupón tras una compra.

Iniciar una campaña por abandono de carrito.

Estos triggers no son de bases de datos, sino de automatizaciones de marketing en plataformas como Mailchimp, Hubspot o ActiveCampaign.

## 9. ¿Cómo hacer un Trigger?

Pasos generales:

Identificar el evento: INSERT, UPDATE o DELETE.

Determinar si el trigger es BEFORE o AFTER.

Escribir la acción que se desea automatizar.

Usar la sintaxis del SGBD (MySQL, PostgreSQL, SQL Server, etc.).

Ejemplo en PostgreSQL
![image](https://github.com/user-attachments/assets/2fe59999-ab13-41d3-814e-a91876d10c5a)

## 10. Características de un Trigger

Se ejecutan automáticamente.

No necesitan ser llamados desde la aplicación.

Se asocian a eventos y tablas/vistas.

Pueden impedir operaciones si contienen validaciones.

Aumentan la seguridad y consistencia de datos.

## 11. Desventajas de un Trigger

Difíciles de depurar (debug).

Ocultan lógica de negocio, lo que puede causar confusión.

Pueden afectar el rendimiento si no se usan con cuidado.

No todos los SGBD los soportan igual.

Mala implementación puede llevar a errores complejos.

## 12. Sustituto de los Trigger en otras bases de datos

Dependiendo del uso, los triggers pueden ser sustituidos por:

Stored Procedures: llamadas desde la aplicación.

ORM Hooks: en frameworks como Django, Laravel, Hibernate.

Middleware: en APIs que validan antes de insertar/actualizar.

Funciones Lambda (en la nube): para operaciones condicionales.

Reglas de integridad referencial y restricciones (CHECK, FOREIGN KEY).


