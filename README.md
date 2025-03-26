# 🤖 Trabajo Final - BotSolution

## 📌 Descripción
Este bot automatiza el proceso de recopilación y envío de todos los trabajos realizados durante el curso de BotSolution. Su propósito es estructurar y enviar la información de los proyectos finalizados junto con el currículum del usuario mediante correo electrónico. 

Este sistema está diseñado para garantizar la correcta documentación de los proyectos, agilizar el proceso de envío y facilitar su revisión.

---

## 🔄 Flujo del Bot
1. **Inicialización**
   - Se obtiene la fecha actual.
   - Se carga la lista de proyectos finalizados.
   - Se valida que los archivos requeridos existan y sean accesibles.

2. **Compilación de la Información**
   - Se genera un archivo ZIP que contiene todos los trabajos finalizados.
   - Se adjunta el currículum del usuario en el paquete final.

3. **Envío por Correo**
   - Se establece conexión con el servidor de correo.
   - Se valida la configuración del email y destinatarios.
   - Se envía el paquete con los archivos adjuntos.
   - Se recibe confirmación de entrega o mensaje de error.

4. **Registro de la Ejecución**
   - Se guarda en la base de datos la fecha y hora del envío.
   - Se almacena el estado de la ejecución para futuras referencias.

---

## 📦 Módulos Utilizados
- `Files` → Para manipulación de archivos y generación del ZIP.
- `Email` → Para el envío automatizado de correos con adjuntos.
- `System` → Para la gestión de variables y ejecución del flujo.
- `Database` → Para almacenar información sobre los envíos realizados.

---

## 📌 Consideraciones
- **Seguridad**: Los datos de acceso al correo deben mantenerse en un entorno seguro.
- **Integridad de Archivos**: Antes del envío, se debe validar que los archivos sean correctos y no estén corruptos.
- **Conectividad**: Se requiere acceso a Internet estable para el correcto envío de los correos.
- **Formato del ZIP**: Todos los archivos deben estar correctamente organizados dentro del ZIP para evitar problemas al recibirlos.

---

## ⚠️ Limitaciones
- **Dependencia de Conexión**: Si la red falla, el correo no se envía.
- **No Implementa Reintentos**: Si el envío falla, no se vuelve a intentar automáticamente.
- **Formato Fijo de Archivos**: No permite agregar archivos fuera de la estructura predefinida.
- **Sin Notificaciones en Tiempo Real**: No informa al usuario en el momento si el envío fue exitoso o fallido.

---

## 🚀 Futuras Mejoras
- Implementar un sistema de reintentos automáticos en caso de fallo.
- Agregar una interfaz visual para la gestión manual de envíos.
- Permitir selección personalizada de archivos antes del envío.
- Integrar un sistema de notificaciones para informar sobre el estado de cada envío.
- Mejorar la seguridad cifrando los datos de acceso al correo.

---

## 📜 Créditos
Desarrollado por **Lautaro Pedernera** como parte del curso de **BotSolutions**.

Agradecimientos especiales a **todo el equipo de BotSolutions** por su apoyo en la finalización de este proyecto.
