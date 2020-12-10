# PRÁCTICA DE MODELADO
# 6 CATÁLOGO DE REQUISITOS DEL SISTEMA A DESARROLLAR

|**ID_01**| **Nombre** |
| :---: | :--- |
|**Descripción**|  |

## 6.1 Requisitos Generales del Sistema
Esta sección debe contener la especificación de los requisitos generales del sistema, también denominados características del sistema (system features) u objetivos del sistema.

## 6.2 Casos de uso del Sistema 
### 6.2.1 Diagramas de Casos de Uso del Sistema
### 6.2.2 Especificación de Actores del Sistema
### 6.2.3 Especificación de Casos de Uso del Sistema

| ID | Nombre |
| :--: | :----- |
|**Precondición**| |
|**Descripción**| |
|**Secuencia Normal**| |
|**Postcondición**| |
|**Excepciones**| |
|**Importancia**| |
|**Prioridad**| |

## 6.3 Requisitos Funcionales del Sistema
Esta sección debe contener los requisitos funcionales del sistema que se hayan identificado a partir de los requisitos generales.

### 6.3.1 Requisitos de Información del Sistema
Estos requisitos deben especificar qué información debe almacenar el sistema para poder ofrecer la funcionalidad descrita en los casos de uso del sistema o en otros requisitos.
  - El sistema almacenará el historial de ubicación de cada teléfono móvil durante 72h.

| ID | Nombre | Descripción |
| :--: | :----- |:----- |
|**RI-01**| | |
 
### 6.3.2 Requisitos de Reglas de Negocio del Sistema
Estos requisitos deben especificar qué reglas de negocio debe respetar el sistema, evitando que se incumplan durante su funcionamiento.
- El almacenamiento de datos deberá cumplir con la ley de protección de datos.
 - El sistema nuevo debe cumplir con las leyes y reglamentos establecidos por cada comunidad autónoma para la protección de datos (legislativo de seguridad y salud).
- El sistema nuevo se acogerá a las leyes generales públicas.
- Solo los usuarios logueados podrán acceder a los datos.
- Cada CCAA utilizará 3 servidores de datos diferentes para almacenar cada copia de los datos.
 - Cada comunidad autónoma gestionará sus propias bases de datos.
  - El sistema solo revelará los datos imprescindible.
- Los sanitarios podrán acceder al historial médico de los pacientes.
- El sistema permitirá a los sanitarios y rastreadores avisar a las fuerzas del orden de ser necesario.
- Los sanitarios y rastreadores deberán avisar a las fuerzas del orden si una persona no acude a una cita médica.
- Los sanitarios y rastreadores deberán avisar a las fuerzas del orden si una persona no cumple la cuarentena asignada.
- Los sanitarios y rastreadores deberán comprobar que los casos diagnosticados como positivos cumplen la cuarentena establecida.

### 6.3.3 Requisitos de Conducta del Sistema
Estos requisitos deben especificar cualquier otro comportamiento deseado del sistema que no se haya especificado mediante los casos de uso del sistema, como generación de informes, funcionalidades transversales a varios casos de uso del sistema, etc.

- El sistema enviará una notificación al usuario para que acuda a realizarse pruebas médicas si ha estado en contacto con un caso positivo.
- El sistema enviará una notificación al usuario si informa de un positivo de un caso cercano o si informa de síntomas compatibles.
- El sistema generará un mapa de calor con los datos de usuarios que hayan sido diagnosticados como positivos.
- El mapa de calor se actualizará cada hora.
- El sistema validará automáticamente los formularios emitidos por el usuario cuando avise de casos positivos cercanos y no dejará enviarlos en caso de que exista algún error.




## 6.4 Requisitos No Funcionales del Sistema

### 6.4.1 Requisitos de Fiabilidad
Estos requisitos deberán establecer, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como recuperabilidad y tolerancia a fallos.
  - Disponibilidad de al menos el 99,99% de las veces.
  - El tiempo de inicio o reinicio del sistema debe ser inferior a un minuto.
  - La probabilidad de fallo será inferior al 3%.
  - El sistema guardará dos copias extras de todos los datos en dos servidores diferentes para evitar pérdidas en caso de caídas del sistema.

### 6.4.2 Requisitos de Usabilidad
Estos requisitos deberán establecer, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como facilidad de aprendizaje, comprensión, operatividad y atractividad.

- El tiempo de aprendizaje del sistema debe ser inferior a 2 horas.
- El sistema debe contar con manuales de usuario y ayuda online.
- El sistema proporcionará errores claros y concisos.
- Los usuarios podrán cambiar el dialecto o el idioma de la aplicación.

### 6.4.3 Requisitos de Eficiencia
Estos requisitos deberán establecer, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como tiempo de respuesta.

- El sistema debe ser capaz de procesar 20 millones de transacciones por minuto.
- Toda transacción debe responder al usuario en menos de 3 segundos.
- El sistema debe soportar 5 millones de conexiones simultáneas.


### 6.4.4 Requisitos de Mantenibilidad
Estos requisitos deberán establecer, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como estabilidad, facilidad de análisis, facilidad de cambio, facilidad de pruebas.
 - El código de la aplicación será publicado en GitHub y sin patentes para que cualquier usuario pueda buscar fallos en la aplicación y ayudar a su mejora.

### 6.4.5 Requisitos de Portabilidad
Estos requisitos deberán establecer, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos relacionados con la escalabilidad: capacidad de instalación, capacidad de sustitución, adaptabilidad, coexistencia, compatibilidad con hardware o software, etc.
  - La aplicación se instalará automaticamente en todos los dispositivos móviles.
  - El uso de está aplicación es compatible con el uso de cualquier otra aplicación.

### 6.4.6 Requisitos de Seguridad
Estos requisitos deberán establecer, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como accesos al sistema, identificación y autenticación, protección de datos y privacidad.
- Los permisos de acceso solo pueden ser modificados por los administradores.
- El sistema debe seguir patrones de seguridad que incrementen la seguridad.
- El sistema debe hacer un backup cada 2h.
- El sistema debe asegurar que los datos están protegidos de accesos no autorizados.


### 6.4.7 Otros Requisitos No Funcionales
Esta sección debe contener los requisitos no funcionales que se hayan identificado y que no pertenezcan a ninguna de las categorías anteriores. 



  
  
## 6.5 Restricciones Técnicas del Sistema
Esta sección debe contener las restricciones técnicas que se imponen al sistema software a desarrollar (tecnología a usar, protocolos de comunicaciones, compatibilidad con navegadores, etc.)
  - La base de datos utilizada será implementada en MySQL.
  - El código de la aplicación estará escrito Kotlin y XML para la parte de cliente, y Java para la parte de servidor.
  - El sistema utilizará la ubicación por GPS y/o por triangulación de antenas móviles.
  - Cualquier intercambio de datos vía Internet que realice el software se realizará por medio del protocolo encriptado HTTPS.
  - Los servidores usados para almacenar datos serán MySQL server, PostgreSQL server y MongoDB server.
  - La aplicación será compatible en todos los SO de los teléfonos móviles y en cualquier navegador.
  - El software podrá ser utilizado en los sistemas operativos Windows, Linux, Android, iOS y HarmonyOS.
  
## 6.6 Requisitos de Integración del Sistema
Estos requisitos deben identificar aquellos servicios disponibles en el entorno tecnológico de producción o componentes software (por ejemplo, librerías enlazables) cuya funcionalidad sea relevante para el sistema a desarrollar y deban ser consumidos por el mismo.

