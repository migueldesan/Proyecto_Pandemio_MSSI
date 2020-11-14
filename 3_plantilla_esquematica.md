# PRACTICA DE MODELADO
# 3 DESCRIPCIÓN DE LA SITUACIÓN ACTUAL 
Aunque la aplicación Radar Covid no nace en España, el Gobierno de España decide comenzar a usar esta aplicación a nivel nacional como parte de las soluciones inmediatas para frenar la pandemia ya que en otros países de la Unión Europea ha tenido bastante éxito. Para usar Radar Covid en cada comunidad autónoma, cada una debía comunicar al Ministerio de Sanidad su uso, que tras comprobar que todo estaba en orden, pidía a la Secretaría de Estado de Inteligencia Artificial (dependiente de Ministerio de Asuntos Económicos) que comienzara la integración técnica. Para la integración técnica, cada comunidad autónoma debía generar un protocolo propio dentro de sus sistemas sanitarios para enviar los códigos a los contagiados -que identifican anónimamente a los positivos y a sus contactos estrechos- y formar a los rastreadores para que puedieran utilizar de mejor manera la información que reciben de la app. Sin embargo, todo este proceso es bastante lento ya que intervienen gran cantidad de actores. 

A día de hoy, Radar Covid ya se está usando a nivel nacional pero no se están conseguido los resultados que se esperaban por diversos motivos como son:
  * El número de descargas de la aplicación es muy bajo ya que es una aplicación de uso voluntario y además se le ha dado poca publicidad en los medios nacionales
  * El conocimiento de la tecnología médica en España es insuficiente.
  * La dificultad para comunicar un positivo. Esto se debe a que los sanitarios deben proporcionar un código para insertar en la aplicación en caso de ser diagnosticado como positivo, y sin embargo muchos sanitarios desconocen la existencia de estos códigos. Además, la colaboración por parte de las Comunidades Autónomas no está siendo la adecuada, y surgen continuamente problemas en la generación de códigos ya que la gestión de los datos entre las diferentes comunidades no está estandarizada.
  * Está basada en el uso de bluetooth. lo que la hace inservible si el bluetooth está apagado o bien, ocupado con los auriculares.
  
Por todo ello y más, nace Pandemio, que tratará de permitirá rastrear y gestionar la información de los ciudadanos de la próxima pandemia de una forma más eficaz.
Para ello es necesario conocer en detalle la situación actual para evitar cometer los mismos errores en Pandemio y mejorar lo que ya existe.

<br>

## 3.1 Pros y contras de la Situación Actual
En esta sección señalaremos los principales aspectos positivos y negativos de Radar Covid con el fin de conservar aquellos que puedan mejorar Pandemio, y corregir aquellos que han llevado al fracaso a Radar Covid para que no suceda lo mismo con Pandemio.

### 3.1.1 Fortalezas de la Situación Actual

Algunos de los aspectos positivos de Radar Covid que convendría que se mantuvieran en Pandemio son los siguientes:

| ID | NOMBRE | DESCRIPCIÓN |
| :---: | :----- | :----- |
| **FO-01** | Anonimato | La aplicación funciona sin revelar la identidad del ciudadano ni la del dispositivo móvil. Además no registra datos personales ni de geolocalización. |
| **FO-02** | Alertas rápidas | Rápido aviso al ciudadano de que ha estado en contacto con un positivo cercano para que comience la cuarentena cuanto antes y disminuya sus contactos sociales. |
| **FO-03** | Discrección | Las alertas de exposición se envían sin indicar el lugar ni momento concreto donde se produjo la exposición. |
| **FO-04** | Encriptación de los datos | Los datos se guardan en cada dispositivo móvil y la conexión con el servidor es privada. |
| **FO-05** | Interfaz amigable | Fácil uso de la interfaz. |
| **FO-06** | Sección de ayuda | Tiene sección de preguntas y enlaces de interés acerca de la enfermedad. |
| **FO-07** | Varios idiomas | Posibilidad de usar la app en varios idiomas. |
| **FO-08** | Gratuita | Es gratuita y fácilmente instalable. |
| **FO-09** | Anonimato | Es posible comunicar de forma anónima el diagnostico positivo de una prueba PCR. |


### 3.1.2 Debilidades de la Situación Actual

Por el contrario, también hay destacar los principales aspectos negativos de Radar Covid que consideramos que no deben repetirse en Pandemio:

| ID | NOMBRE | DESCRIPCIÓN |
| :---: | :----- | :----- |
| **DE-01** | Descarga y uso voluntario | La instalación y el uso de la aplicación no son obligatorios lo que dificulta el rastreo del virus en la población ya que solo un pequeño porcentaje de la población la usa diariamente. |
| **DE-02** | Sanitarios poco familiarizados con la App | No todo el personal sanitario está familiarizado con el funcionamiento de la app y pocos hacen uso de ella. |
| **DE-03** | Desconocimiento de la App | Gran parte de la población no conoce la existencia de la aplicación. |
| **DE-04** | Vulnerabilidad a ataques | El uso del Bluetooth provoca que los dispositivos móviles sean más vulnerables a ataques informáticos. |
| **DE-05** | Funcionamiento basado en Bluetooth | La aplicación hace uso del Bluetooth para su correcto funcionamiento y generalmente suele estar apagado u ocupado por otros dispositivos. Esto provoca que las aplicaciones actuales no funcionen correctamente y que el rastreo del virus sea aún más complicado. |
| **DE-06** | Incompatibilidad entre Apps | El uso del Bluetooth en varias aplicaciones puede generar problemas de incompatibilidad entre ellas y que los sistemas software no funcionen correctamente. |
| **DE-07** | Desconocimiento del Bluetooth | Mucha gente mayor no conoce como funciona el Bluetooth por lo que las aplicaciones que se basan en Bluetooth pierden su potencial. 
| **DE-08** | Desconocimiento del propio dispositivo móvil| Mucha gente de avanzada edad desconoce como descargar aplicaciones en su móvil y su uso. |
| **DE-09** | Nula estandarización | Las bases de datos de las diferentes administraciones no estan estandarizadas lo que provoca que muchos usuarios no puedan informar de sus positivos si se mueven entre distintas comunidades. |

<br>


## 3.2	Modelos de Procesos de Negocio Actuales

En esta sección trataremos de señalar los principales modelos de negocio que existen en la actualidad.

### 3.2.1 Descripción de los Actores de Negocio Actuales

Los actores de negocio son los siguientes: 

* Secretaría de Estado de Digitalización e Inteligencia Artificial del Gobierno de España: Son competencias de esta Secretaría de Estado las relativas a la política de impulso a la digitalización de la sociedad y economía, a través del fomento y regulación de los servicios digitales y de la economía y sociedad digitales, la interlocución con los sectores profesionales, industriales y académicos, así como el impulso de la digitalización del sector público.

* Sanitarios: Persona que trabaja en la sanidad tanto en todas las comunidades autónomas.

* Ministerio de Sanidad: Es el Departamento de la Administración General del Estado que asume la propuesta y ejecución de la política del Gobierno de la Nación en materia de salud, de planificación y asistencia sanitaria, así como el ejercicio de las competencias de la Administración General del Estado para asegurar a los ciudadanos el derecho a la protección de la salud.

* Gobierno de España: Es el órgano constitucional que encabeza el poder ejecutivo del Reino de España y dirige la Administración General del Estado. Según la Constitución española, sus funciones son dirigir la política interior y exterior, la administración civil y militar y la defensa del Estado; así como de ejercer la función ejecutiva y la potestad reglamentaria de acuerdo con la Constitución y las leyes.

* Comunidad europea: es una comunidad política de derecho constituida en régimen sui géneris de organización internacional nacida para propiciar y acoger la integración y gobernanza en común de los Estados y los pueblos de Europa. Está compuesta por veintisiete paises europeos.

| **info_01** | **Actores de negocio**
--- | --- 
| **Versión** | 1.0 (13-11-2020) 
| **Dependencías** |  * La comunidad europea deberá tener un acuerdo con los paises 
| **Descripción** | Esta sección contiene información sobre los actores de negocio de los modelos de los procesos de negocio.
| **Comentarios** | 

## 3.3 ENTORNO TECNOLÓGICO ACTUAL

**HARDWARE**
* Smartphones para la ejecución de la aplicación, servidores para soportarla, PC para gestionar los códigos en caso de positivo (coordinado con servicios médicos), PC para la administración de la aplicación. 

### 3.3.2 Descripción del Entorno de Software Actual

El entorno software de Radar Covid es bastante simple: se trata de una aplicación movil disponible en Android e iOs y para su correcto funcionamiento es necesario el uso del Bluetooth. 
La gestión de los datos está basada en el modelo descentralizado ya que los datos de cada ciudadano se guardan en cada dispositivo móvil y la conexión con el servidor es privada para garantizar el anonimato y la confidencialidad de los ciudadanos.


* Necesidad de que el smartphone del cliente cuente con Bluetooth y servicio GPS. 
* Aplicación móvil disponible en Android e iOS. 
* Programa generador de código destinado a uso sanitario.
