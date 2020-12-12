# PRÁCTICA DE MODELADO
# 6 CATÁLOGO DE REQUISITOS DEL SISTEMA A DESARROLLAR

## 6.1 Requisitos Generales del Sistema
Esta sección debe contener la especificación de los requisitos generales del sistema, también denominados características del sistema (system features) u objetivos del sistema.

<br>

## 6.2 Casos de uso del Sistema 
### 6.2.1 Diagramas de Casos de Uso del Sistema

> Casos de uso sanitarios y rastreadores
<p align="center">
  <img src="./Imágenes/Casos_de_uso_sanitarios.jpg">
</p>

> Casos de uso fuerzas del orden
<p align="center">
  <img src="./Imágenes/Casos_de_uso_fuerzas_del_orden.jpg">
</p>

> Casos de uso Gobierno de España
<p align="center">
  <img src="./Imágenes/Casos_de_uso_gobierno.jpg">
</p>

> Casos de uso usuarios anónimos
<p align="center">
  <img src="./Imágenes/Casos_de_uso_usuario_anonimo.jpg">
</p>







### 6.2.2 Especificación de Actores del Sistema
### 6.2.3 Especificación de Casos de Uso del Sistema

| CU_02 | Ver avisos fuerzas del orden |
| :--: | :----- |
|**Precondición**| El sanitario ha avisado previamente a las fuerzas del orden para informarles de un caso que no está cumpliendo la cuarentena o no ha asistido a una cita médica. Además, el sanitario debe estar logueado en la aplicación. |
|**Descripción**| Un sanitario/rastreador puede ver los avisos que han emitido las fuerzas del orden sobre un caso que ha abierto el sanitario previamente. |
|**Secuencia Normal**| 1. El sanitario abre la aplicación. <br> 2. El sanitario elige la opción “Ver avisos fuerzas del orden”. <br> 3. La aplicación muestra todos los avisos que hayan emitido las fuerzas del orden sobre casos abiertos previamente por el sanitario. <br> 4. El sanitario abre un aviso para ver los detalles y las nuevas noticias sobre el caso. |
|**Postcondición**| Ninguna. |
|**Excepciones**| 3a. Si el sanitario no tiene ningún caso abierto se muestra una lista vacía.  |
|**Importancia**| Alta. |
|**Prioridad**| Alta. |


| CU_06 | Ver citas médicas propias |
| :--: | :----- |
|**Precondición**| Un usuario está pendiente de acudir a una cita médica. |
|**Descripción**| Un usuario de la aplicación de Pandemio puede ver la fecha, hora y lugar de la cita médica que tiene asignada. |
|**Secuencia Normal**| 1. El usuario abre la aplicación. <br> 2. El usuario elige la opción “Ver citas médicas propias”. <br> 3. La aplicación muestra la fecha, hora y lugar donde debe acudir a la cita médica. |
|**Postcondición**| Ninguna. |
|**Excepciones**| 3a. Si el usuario no tiene que cumplir ninguna cita médica asignada se muestra un mensaje avisándole.  <br> 3b. Si el usuario ha informado de un caso cercano positivo sin móvil, el sistema especificará en el mensaje quién debe acudir a la cita médica. |
|**Importancia**| Alta. |
|**Prioridad**| Alta. |


| CU_07 | Ver cuarentena establecida |
| :--: | :----- |
|**Precondición**| Un usuario está pendiente de realizarse pruebas médicas o se le ha establecido una cuarentena sanitaria. |
|**Descripción**| Un usuario de la aplicación de Pandemio puede ver cuantos días de cuarentena tiene que realizar. |
|**Secuencia Normal**| 1. El usuario abre la aplicación. <br> 2. El usuario elige la opción “Ver cuarentena establecida”. <br> 3. La aplicación muestra el número de días que quedan de cuarentena y la fecha en la que termina. |
|**Postcondición**| Ninguna. |
|**Excepciones**| 3a. Si el usuario no tiene que cumplir ninguna cuarentena se muestra un mensaje avisándole.  <br> 3b. Si el usuario ha informado de un caso cercano positivo sin móvil, el sistema especificará en el aviso quién debe cumplir la cuarentena establecida y hasta que fecha. |
|**Importancia**| Alta. |
|**Prioridad**| Alta. |



| CU_08 | Informar de caso cercano positivo sin móvil |
| :--: | :----- |
|**Precondición**| Un usuario tiene a su cargo a una persona que no dispone de teléfono móvil. |
|**Descripción**| Un usuario de la aplicación de Pandemio puede informar de un caso positivo para una persona que no dispone de teléfono móvil. |
|**Secuencia Normal**| 1. El usuario abre la aplicación. <br> 2. El usuario elige la opción “Informar de caso cercano positivo sin móvil”. <br> 3. El usuario rellena los datos que pide la aplicación. <br> 4. El usuario envía el formulario. <br> 5. La aplicación comprueba que los datos introducidos son correctos. <br> 6. La aplicación procesa el formulario y genera una cita médica. <br> 7. La aplicación muestra un mensaje con la cita médica creada. |
|**Postcondición**| Se ha creado una cita médica que se puede ver en la opción “Ver citas médicas propias”. |
|**Excepciones**| 6. El formulario está mal rellenado o contiene algún error. <br> &nbsp;&nbsp;&nbsp; 6.1. La aplicación muestra un mensaje de error con el motivo del fallo. <br> &nbsp;&nbsp;&nbsp; 6.2. Volver al paso 3. |
|**Importancia**| Media. |
|**Prioridad**| Baja. |

| CU_09 | Informar de síntomas compatibles |
| :--: | :----- |
|**Precondición**| Un usuario comienza a tener síntomas compatibles con la nueva pandemia. |
|**Descripción**| Un usuario de la aplicación de Pandemio puede informar de que comienza a desarrollar síntomas compatibles con la nueva enfermedad. |
|**Secuencia Normal**| 1. El usuario abre la aplicación. <br> 2. El usuario elige la opción “Informar de síntomas compatibles”. <br> 3. El usuario rellena los datos que pide la aplicación. <br> 4. El usuario envía el formulario. <br> 5. La aplicación comprueba que los datos introducidos son correctos. <br> 6. La aplicación procesa el formulario y genera una cita médica. <br> 7. La aplicación muestra un mensaje con la cita médica creada. |
|**Postcondición**| Se ha creado una cita médica que se puede ver en la opción “Ver citas médicas propias”. |
|**Excepciones**| 6. El formulario está mal rellenado o contiene algún error. <br> &nbsp;&nbsp;&nbsp; 6.1. La aplicación muestra un mensaje de error con el motivo del fallo. <br>&nbsp;&nbsp;&nbsp; 6.2. Volver al paso 3. |
|**Importancia**| Media. |
|**Prioridad**| Baja. |

| CU_10 | Ver mapa calor |
| :--: | :----- |
|**Precondición**| Ninguna. |
|**Descripción**| Un usuario de la aplicación de Pandemio puede ver un mapa de calor con para ver las zonas donde ha habido un gran número de casos positivos y así evitar esas zonas. |
|**Secuencia Normal**| 1. El usuario abre la aplicación. <br> 2. El usuario elige la opción “Ver mapa de calor”. <br> 3. El sistema muestra un mapa de calor de la zona donde se encuentra el usuario acompañado con una leyenda de colores para ver el impacto de la nueva pandemia en la zona. |
|**Postcondición**| Ninguna.  |
|**Excepciones**| Ninguna. |
|**Importancia**| Media. |
|**Prioridad**| Media. |


| CU_11 | Enviar ubicación |
| :--: | :----- |
|**Precondición**| Un sanitario o rastreador solicita a un usuario que mande la ubicación donde se encuentra. |
|**Descripción**| Un usuario de la aplicación de Pandemio debe mandar la ubicación donde se encuentra para confirmar que está cumpliendo la cuarentena si un sanitario o rastreador se lo pide. |
|**Secuencia Normal**| 1. El usuario abre la aplicación. <br> 2. El usuario elige la opción “Enviar ubicación”. <br> 3. El usuario coloca su huella en el sensor de huellas del teléfono móvil. <br> 4. La aplicación valida la huella colocada. <br> 5. La aplicación envía la ubicación del teléfono móvil al sanitario o rastreador correspondiente.  |
|**Postcondición**| Ubicación enviada correctamente.  |
|**Excepciones**| 3. El usuario utiliza el reconocimiento facial de su teléfono móvil. <br> &nbsp;&nbsp;&nbsp; 3.1. La aplicación valida la cara reconocida. <br> &nbsp;&nbsp;&nbsp; 3.2. La aplicación envía la ubicación del teléfono móvil al sanitario o rastreador correspondiente. <br> 4. La huella o la cara introducidas no se corresponden con el usuario que ha solicitado el sanitario. <br> &nbsp;&nbsp;&nbsp; 4.1. La aplicación muestra un mensaje de error con el motivo del fallo. <br> &nbsp;&nbsp;&nbsp; 4.2. Volver al paso 3. |
|**Importancia**| Alta. |
|**Prioridad**| Alta. |


<br>

## 6.3 Requisitos Funcionales del Sistema
Esta sección debe contener los requisitos funcionales del sistema que se hayan identificado a partir de los requisitos generales.

### 6.3.1 Requisitos de Información del Sistema
Estos requisitos deben especificar qué información debe almacenar el sistema para poder ofrecer la funcionalidad descrita en los casos de uso del sistema o en otros requisitos.
Describen qué información debe almacenar el sistema para poder ofrecer los servicios necesarios.

  - El sistema almacenará el historial de ubicación de cada teléfono móvil el número de días que establezcan los criterios estrictamente epidemiológicos.
  - El sistema almacenará la ubicación obtenida por medio de la triangulación de antenas móviles si se puede conseguir un margen de error de menos de 5 metros, en cualquier oto caso almacenará la obtenida por medio del GPS.
   - Cuando el teléfono móvil esté en modo avión solo almacenará la ubicación obtenida por medio del GPS.

| **ID** | **Nombre** | **Descripción** |
| :--: | :----- |:----- |
|**RI-01**| | |

 
### 6.3.2 Requisitos de Reglas de Negocio del Sistema
Estos requisitos deben especificar qué reglas de negocio debe respetar el sistema, evitando que se incumplan durante su funcionamiento.
Describen restricciones, reglas o políticas del negocio que deben ser respetadas por el sistema a desarrollar.

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
Describen los servicios que debe ofrecer el sistema para que los usuarios u otros sistemas puedan realizar sus tareas de negocio:

- El sistema generará citas médicas automáticas para el centro de salud más cercano cuando una persona haya estado en contacto con un positivo, o se informe de un positivo de un caso cercano sin teléfono móvil o se informe de síntomas compatibles.
- El sistema enviará una notificación PUSH al usuario para que acuda a realizarse pruebas médicas si ha estado en contacto con un caso positivo.
- El sistema enviará una notificación PUSH al usuario para que acuda a realizarse pruebas médicas si informa de un positivo de un caso cercano sin teléfono móvil o si informa de síntomas compatibles.
- El sistema enviará una notificación PUSH a los usuarios que deban realizar la cuarentena informandoles del número de días de cuarentena que deben cumplir. 
- El sistema generará un mapa de calor con los datos de usuarios que hayan sido diagnosticados como positivos.
- El mapa de calor se actualizará cada hora.
- El número mínimo de personas contagiadas que deben pasar por una zona para que está aparezca coloreada en el mapa de calor será de 5 personas.
- El mapa de calor se coloreará con colores que vayan desde el amarillo hasta el rojo en función del número de casos positivos que haya en la zona.
- El sistema validará automáticamente los formularios emitidos por el usuario cuando avise de casos positivos cercanos y no dejará enviarlos en caso de que exista algún error.
- El sistema notificará a las CCAA si un caso positivo se ha movido entre comunidades.
- El sistema generará un informe con los casos positivos que hayan salido del país para comunicarselo lo antes posible.
- El sistema generará un informe con los datos obtenidos por el mapa de calor y solo podrá acceder a él el Gobierno.

<br>

## 6.4 Requisitos No Funcionales del Sistema

### 6.4.1 Requisitos de Fiabilidad
Estos requisitos deberán establecer, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como recuperabilidad y tolerancia a fallos.
  - Disponibilidad de al menos el 99,99% de las veces.
  - El tiempo de inicio o reinicio del sistema debe ser inferior a dos minutos.
  - La probabilidad de fallo será inferior al 3%.
  - El sistema guardará dos copias extras de todos los datos en dos servidores diferentes para evitar pérdidas en caso de caídas del sistema.

### 6.4.2 Requisitos de Usabilidad
Estos requisitos deberán establecer, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como facilidad de aprendizaje, comprensión, operatividad y atractividad.

- El tiempo de aprendizaje del sistema debe ser inferior a 2 horas.
- El sistema debe contar con manuales de usuario y ayuda online.
- El sistema proporcionará errores claros y concisos.
- Los usuarios podrán cambiar el dialecto o el idioma de la aplicación.
- El sistema deberá permitir en el 80% de las veces que con un máximo de 5 clicks sea suficiente para llegar a la información deseada.

### 6.4.3 Requisitos de Eficiencia
Estos requisitos deberán establecer, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como tiempo de respuesta.

- El sistema debe ser capaz de procesar 20 millones de transacciones por minuto.
- Toda transacción debe responder al usuario en menos de 10 segundos.
- El sistema debe soportar 5 millones de conexiones simultáneas.
- El sistema deberá tener un tiempo máximo de respuesta de 5 segundos para cualquier operación de consulta.


### 6.4.4 Requisitos de Mantenibilidad
Estos requisitos deberán establecer, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como estabilidad, facilidad de análisis, facilidad de cambio, facilidad de pruebas.
 - El código de la aplicación será publicado en GitHub y sin patentes para que cualquier usuario pueda buscar fallos en la aplicación y ayudar a su mejora.
 - Se forzará la actualización de la aplicación si se identifica algún bug que pueda afectar al sistema.
 - El código fuente que se implemente en JAVA deberá cumplir las recomendaciones de Code Conventions for the Java Programming Language

### 6.4.5 Requisitos de Portabilidad
Estos requisitos deberán establecer, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos relacionados con la escalabilidad: capacidad de instalación, capacidad de sustitución, adaptabilidad, coexistencia, compatibilidad con hardware o software, etc.
  - La aplicación se instalará automaticamente en todos los dispositivos móviles.
  - El uso de está aplicación es compatible con el uso de cualquier otra aplicación.
  - El sistema deberá evitar el uso de extensiones propietarias al estándar SQL-92 en el sistema de gestión de bases de datos que utilice.

### 6.4.6 Requisitos de Seguridad
Estos requisitos deberán establecer, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como accesos al sistema, identificación y autenticación, protección de datos y privacidad.
- Los permisos de acceso solo pueden ser modificados por los administradores.
- El sistema debe seguir patrones de seguridad que incrementen la seguridad.
- El sistema debe hacer un backup cada 2h.
- El sistema debe asegurar que los datos están protegidos de accesos no autorizados.
- El sistema controlará el acceso y lo permitirá solamente a usuarios autorizados.
- Los usuarios accederán al sistema con un nombre de usuario y contraseña.
- El sistema enviará una alerta a los administradores del sistema cuando ocurra alguno de los siguientes eventos: entrada al sistema por parte de un usuario, 2 o más intentos fallidos al introducir la contraseña de usuario y cambio de contraseña de usuario.
- El sistema deberá ser capaz de evitar ataques de inyección de SQL sistemáticos.


### 6.4.7 Otros Requisitos No Funcionales
Esta sección debe contener los requisitos no funcionales que se hayan identificado y que no pertenezcan a ninguna de las categorías anteriores. 
  - No será necesario tener la aplicación abierta para que funcione correctamente.
 - La aplicación debe contar con dos formularios, uno para informar de un caso positivo cercano de una persona dependiente, y otro para informar de síntomas compatibles. Estos formularios no se podrán enviar si contienen algún error y será el propio sistema el encargado de gestionarlos.

<br>
  
## 6.5 Restricciones Técnicas del Sistema
Esta sección debe contener las restricciones técnicas que se imponen al sistema software a desarrollar (tecnología a usar, protocolos de comunicaciones, compatibilidad con navegadores, etc.)
  - El motor de la base de datos donde se almacenará toda la información será MySQL.
  - El código de la aplicación estará escrito Kotlin y XML para la parte de cliente, y Java para la parte de servidor.
  - El sistema utilizará la ubicación por GPS y/o por triangulación de antenas móviles.
  - Cualquier intercambio de datos vía Internet que realice el software se realizará por medio del protocolo encriptado HTTPS.
  - Los servidores usados para almacenar datos serán MySQL server, PostgreSQL server y MongoDB server.
  - La aplicación será compatible en todos los SO de los teléfonos móviles y en cualquier navegador.
  - El software podrá ser utilizado en los sistemas operativos Windows, Linux, Android, iOS y HarmonyOS.
  
<br>  
  
## 6.6 Requisitos de Integración del Sistema
Estos requisitos deben identificar aquellos servicios disponibles en el entorno tecnológico de producción o componentes software (por ejemplo, librerías enlazables) cuya funcionalidad sea relevante para el sistema a desarrollar y deban ser consumidos por el mismo.
 - El sistema deberá utilizar el servicio @firma para todos los aspectos relacionados con validación y firma electrónica.
