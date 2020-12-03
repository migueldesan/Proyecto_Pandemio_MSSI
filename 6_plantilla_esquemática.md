# PRÁCTICA DE MODELADO
# 6 CATÁLOGO DE REQUISITOS DEL SISTEMA A DESARROLLAR

## 6.3 Requisitos Funcionales del Sistema

- El sistema enviará una notificación al usuario para que acuda a realizarse pruebas médicas si ha estado en contacto con un caso positivo.
- El sistema permitirá a los sanitarios y rastreadores avisar a las fuerzas del orden de ser necesario.
- El sistema validará automáticamente los formularios emitidos por el usuario y no dejará enviarlos en caso de que exista algún error.
- La base de datos utilizada será implementada en MySQL.
- Cada comunidad autónoma gestionará sus propias bases de datos.


## 6.4 Requisitos No Funcionales del Sistema

### 6.4.2 Requisitos de Usabilidad
- El tiempo de aprendizaje del sistema debe ser inferior a 2 horas.
- El sistema debe contar con manuales de usuario y ayuda online.
- El sistema proporcionará errores claros y concisos.
- El software podrá ser utilizado en los sistemas operativos Windows, Linux, Android, iOS y HarmonyOS.
- Selección de idioma.

### 6.4.3 Requisitos de Eficiencia
- El sistema debe ser capaz de procesar N transacciones por minuto.
- Toda transacción debe responder al usuario en menos de 3 segundos.
- El sistema debe soportar 5 millones de conexiones simultáneas.

### 6.4.6 Requisitos de Seguridad
- Los permisos de acceso solo pueden ser modificados por los administradores.
- El sistema debe seguir patrones de seguridad que incrementen la seguridad.
- El sistema debe hacer un backup cada 2h.
- El sistema debe asegurar que los datos están protegidos de accesos no autorizados.
- Cualquier intercambio de datos vía Internet que realice el software se realizará por medio del protocolo encriptado HTTPS.

### 6.4.7 Otros Requisitos No Funcionales
- Dependibilidad:
  - Disponibilidad de al menos el 99,99% de las veces.
  - Tiempo de inicio o reinicio del sistema debe ser inferior a un minuto.
  - La probabilidad de fallo sera inferior al 3%.
- Externos:
  - El sistema nuevo debe cumplir con las leyes y reglamentos establecidos por cada comunidad autónoma para la protección de datos (legislativo de seguridad y salud).
  - El sistema nuevo se acogerá a las leyes generales públicas, será gratuito, de código abierto, publicado en GitHub y sin patentes (regulatorio).
  - El sistema solo revelará los datos imprescindibles. (regulatorio).
  
