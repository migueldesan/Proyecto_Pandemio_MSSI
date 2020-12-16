<h1 align="center">
   PRÁCTICA DE MODELADO: PANDEMIO
</h1>

<br><br>
<p align="center">
  <img width=100% src="./Imágenes/logo_uva.jpeg">
</p>
<br><br>

<p align="right">
  RAMOS MARTÍNEZ, JOSEBA <br>
  VEGANZONES CARRASCAL, DANIEL<br>
  DE SANTIAGO GILSANZ, MIGUEL
</p>
<br><br>


# ÍNDICE
1. INTRODUCCIÓN.
   1. Alcance.
   2. Objetivos.
2. INFORMACIÓN DEL DOMINIO DEL PROBLEMA.
   1. Introducción al Dominio del Problema.
   2. Glosario de Términos.
3. DESCRIPCIÓN DE LA SITUACIÓN ACTUAL.
   1. Pros y Contras de la Situación Actual.
      1. Fortalezas de la Situación Actual.
      2. Debilidades de la Situación Actual.
   2. Modelos de Procesos de Negocio Actuales.
      1. Descripción de los Actores de Negocio Actuales.
      2. Descripción de Procesos de Negocio Actuales.
   3. Entorno Tecnológico Actual.
      1. Descripción del Entorno de Hardware Actual.
      2. Descripción del Entorno de Software Actual.
4. NECESIDADES DE NEGOCIO.
   1. Objetivos de Negocio.
   2. Modelos de Procesos de Negocio a Implantar.
       1. Descripción de los Actores de Negocio a Implantar.
       2. Descripción de Procesos de Negocio a Implantar.
5. DESCRIPCIÓN DE LOS SUBSISTEMAS DEL SISTEMA A DESARROLLAR.
6. CATÁLOGO DE REQUISITOS DEL SISTEMA A DESARROLLAR.
   1. Requisitos Generales del Sistema.
   2. Casos de uso del Sistema.
       1. Diagramas de Casos de Uso del Sistema.
       2. Especificación de Actores del Sistema.
       3. Especificación de Casos de Uso del Sistema.
   3. Requisitos Funcionales del Sistema.
       1. Requisitos de Información del Sistema.
       2. Requisitos de Reglas de Negocio del Sistema.
       3. Requisitos de Conducta del Sistema.
   4. Requisitos No Funcionales del Sistema.
       1. Requisitos de Fiabilidad.
       2. Requisitos de Usabilidad.
       3. Requisitos de Eficiencia.
       4. Requisitos de Mantenibilidad.
       5.	Requisitos de Portabilidad.
       6.	Requisitos de Seguridad.
       7.	Otros Requisitos No Funcionales.
   5. Restricciones Técnicas del Sistema.
   6.	Requisitos de Integración del Sistema.
   7.	Información Sobre Trazabilidad.
  
<br>

# 1 INTRODUCCIÓN
A finales de diciembre de 2019 se identificaron en Wuhan, en la provincia china de Hubei, 41 casos de neumonía. Un análisis más exhaustivo mostró que se trataba de un nuevo caso de coronavirus que fue denominado SARS-CoV-2, o como comúnmente se conoce, Covid-19.

Cuando se detectaron los primeros casos, nadie podía imaginar que, unos meses más tarde, concretamente el 11 de marzo de 2020, la Organización Mundial de la Salud (OMS) declararía que el nuevo brote de coronavirus constituía una pandemia debido a que esta nueva enfermedad ya estaba presente en los seis continentes del planeta.

Actualmente hay más de 50 millones de casos confirmados en todo el planeta (y más de un millón de muertos relacionados con esta enfermedad) por lo que los países han tenido que tomar diferentes medidas como los cierres de fronteras o el confinamiento de la población para intentar aplanar la curva de incidencia del virus y evitar su rápida propagación. 

Además, ahora que se van conociendo más detalles de esta nueva enfermedad: cómo se propaga, cómo podemos reducir el número de contagios, síntomas relacionados, etc., están surgiendo diferentes sistemas software, como Radar Covid, para rastrear y gestionar la información de los ciudadanos con el fin de aplanar la curva de incidencia e intentar erradicar esta pandemia o posibles pandemias que surjan en el futuro. 

Sin embargo, ninguna de las aplicaciones actuales está teniendo los resultados que se esperaban ya que ninguna es obligatoria o se basan en software que no toda la población conoce, y por este motivo nace la aplicación de Pandemio.

Pandemio será una plataforma que permitirá rastrear y gestionar la información de los ciudadanos de la próxima pandemia con el fin de reducir el impacto de la pandemia en la población y así evitar tomar decisiones extremas como el confinamiento domiciliario de la población.

En este documento se especifican los aspectos más destacados de Pandemio, confiando en que sirvan como punto de partida para llevar a cabo un análisis detallado de los requisitos de este proyecto. Esta especificación de requisitos debe ser suficientemente precisa como para afrontar, en fases posteriores, el diseño y la implementación del proyecto.

<br>

## 1.1 Alcance
Dado que lo que se busca con esta aplicación es el control total sobre el contagio y expansión de la pandemia, se buscará alcanzar al máximo de la población posible, en este caso el 100% de las personas que utilizan teléfonos móviles.

Deberemos para ello crear una nueva aplicación móvil que llamaremos Pandemio y llevar a cabo un proceso judicial con el objetivo de que Pandemio sea instalada en todos los teléfonos móviles de forma obligatoria, ya sea a través de Google en los Android, o de Apple en dispositivos iOS.

Una vez tengamos la certeza de que la aplicación está instalada en todos los teléfonos móviles, el objetivo es controlar a las personas diagnosticadas como positivas en la próxima pandemia y a las personas a las que hayan podido contagiar, usando para ello la ubicación del teléfono, o en su defecto, por medio de una triangulación a través de las antenas de telefonía móvil siempre que se pueda obtener un margen de error pequeño a la hora de ubicar a las personas. En cualquier caso, se descarta el uso del Bluetooth por todos los inconvenientes que genera en las aplicaciones móviles que existen actualmente.

Por otro lado, habrá que considerar la posibilidad de que un caso positivo en la próxima pandemia o un contacto estrecho se desplace entre comunidades autónomas o incluso a otros países. La aplicación tendrá bases de datos independientes para cada comunidad autónoma ya que la gestión de la sanidad en cada una de ellas es diferente, por lo que en caso de que se produzca un desplazamiento de este tipo se deberá advertir a los sistemas sanitarios de aquellos lugares a los que se ha desplazado el caso positivo. En caso de permanecer en España podremos seguir su movimiento a través de Pandemio, pero en caso de salir a otro país se avisará a las autoridades sanitarias del país correspondiente y pasaría a ser de su responsabilidad.

Desde Pandemio se crearán citas médicas automáticas para que los contactos estrechos de un caso positivo acudan a realizarse las pruebas médicas oportunas, y en caso de que no acudan, se informará a las fuerzas del orden (policía local, nacional, guardia civil o al ejército) para que vayan a investigar el motivo. Además, desde Pandemio se tratará de controlar si un caso positivo está cumpliendo o no la cuarentena.

Surge también el problema en cuanto al rastreo de personas que no utilizan teléfonos móviles. Tenemos que aceptar este hecho, intentando tener cierto seguimiento a través de sus familiares o personas cercanas, por lo que se incluirá la posibilidad de informar de un caso positivo/sospechoso por si una persona tiene a su cargo a otra que no dispone de teléfono móvil. Esto supone que el personal sanitario y las fuerzas del orden deberán tener un mayor control sobre este grupo de población. 

Siendo conscientes de que el rastreo de la ubicación y los movimientos de la población puede verse como una invasión a su intimidad, nos comprometemos a respetar en todo momento la Ley de Protección de Datos y a almacenar los datos de cada usuario solo el tiempo que sea necesario para el rastreo de la enfermedad. A los datos sanitarios solo tendrán acceso el personal sanitario y las fuerzas del orden, mientras que los usuarios de Pandemio solo podrán ver un mapa de calor con las zonas por las que se ha movido una persona con diagnóstico positivo, pero siempre respetando el anonimato y la confidencialidad de los usuarios de la aplicación.

En cuanto al mantenimiento y actualizaciones de la aplicación, el objetivo inicial es obtener un producto final por lo que no serían necesarias, aunque Pandemio estaría abierto a versiones y actualizaciones en caso de necesidad.

<br>

## 1.2 Objetivos
En la siguiente tabla se describen los principales objetivos que se esperan alcanzar con Pandemio cuando se termine de implementar:
 | ID | OBJETIVO |
 | :--: | :----- |
 | **OB_01** | Mejorar las aplicaciones software existentes en la lucha contra una futura pandemia. |
 | **OB_02** | Alcanzar el 100% de la población que disponga de teléfonos móviles. |
 | **OB_03** | Alcanzar el mayor número de población posible. |
 | **OB_04** | Rastrear y gestionar la información de los usuarios de forma anónima. |
 | **OB_05** | Preservar la privacidad de los usuarios. |
 | **OB_06** | Reducir el impacto de futuras pandemias en la sociedad. |
 | **OB_07** | Automatizar el proceso de citaciones para realizar pruebas médicas. |
 | **OB_08** | Informar a los usuarios que deben acudir a realizarse pruebas médicas. |
 | **OB_09** | Avisar a las fuerzas del orden si un usuario no acude a realizarse las pruebas médicas. |
 | **OB_10** | Avisar a las fuerzas del orden si un usuario no cumple con la cuarentena que se le ha impuesto. |
 | **OB_11** | Verificar de forma automática que los usuarios cumplen las cuarentenas impuestas. |
 | **OB_12** | Rastrear a los contactos estrechos de los usuarios. |
 | **OB_13** | Mostrar un mapa de calor con las zonas de movilidad de los casos positivos. |
 | **OB_14** | Coordinación entre CCAA y países. |
 
 
 <br>
 <br>
 
 # 2 INFORMACIÓN DEL DOMINIO DEL PROBLEMA
Desde comienzos del año 2020 el mundo se encuentra sumergido en una pandemia global debido al coronavirus COVID-19. Actualmente, en España, como modo de rastreo del virus y como ayuda a los ciudadanos, se han creado diferentes sistemas software para intentar reducir el impacto que está provocando esta pandemia, pero sin los resultados que se esperaban.
Pandemio tratará de mejorar los sistemas existentes para que en una futura pandemia estemos más preparados para combatirla, para que el alcance de reproducción de la enfermedad disminuya (y con ello el número de contagios y muertes provocadas por ella) y no sea necesario tomar medidas extremas como el confinamiento domiciliario de todo el país lo que supondría un desastre económico y el empobrecimiento de la población.

<br>

## 2.1 Introducción al Dominio del Problema
Para la pandemia en la que nos encontramos, cuando una persona comienza a presentar síntomas de la enfermedad o ha estado en contacto con una persona diagnosticada como positiva, debe permanecer en cuarentena y acudir al centro de salud para realizarse pruebas médicas. Estas pruebas consisten en realizarse un test rápido (que en caso de dar positivo se confirma que la persona presenta el coronavirus) y/o una PCR para confirmar los resultados obtenidos por el test rápido si se ha obtenido un negativo o no se lo ha realizado por algún motivo. Además, aunque se obtenga una PCR negativa, es necesario realizar una cuarentena de unos 10 días para evitar posibles falsos negativos. A los 10 días se realiza una nueva PCR para poder dar el alta médica a esa persona.
En la actualidad todo este proceso de citación y rastreo de personas se realiza de forma manual, en cambio, con Pandemio se tratará de automatizar todo el proceso. Además, el cumplimiento de la cuarentena no se puede verificar por ningún medio efectivo que no conlleve un gran gasto de tiempo por parte del personal sanitario o de los cuerpos de policía, por lo que Pandemio se intentará automatizar en los casos que sea posible (con huella dactilar o por reconocimiento facial con el teléfono móvil, enviando ubicación a horas aleatorias, etc.).

<br>


## 2.2 Glosario de términos

A continuación, se presenta una lista ordenada alfabéticamente con los principales términos, acrónimos y abreviaturas específicos del dominio del problema.

<img align="right" width=35% src="./Imágenes/aplaneamiento-de-cuerva.png">

* **Aplanar la curva de incidencia:** El objetivo para luchar contra una enfermedad es reducir el número de contagiados. La curva de la gráfica de contagio se aplana cuando deja de crecer el número de contagiados y se dibuja algo así como una 'meseta'. Es la forma gráfica de ver que, durante un periodo de tiempo, el número de contagios se mantiene y no se incrementa, lo que significa que la velocidad de los contagios es menor y, por tanto, que se ha frenado la tendencia al alza. El aislamiento sanitario, las pruebas médicas y las medidas sanitarias que se toman tienen como intención aplanar la curva de contagios.

<img align="right" width=20% src="./Imágenes/bluetooth.png">

* **Bluetooth:** Especificación industrial para redes inalámbricas de área personal (WPAN) creado por Bluetooth Special Interest Group, Inc. que posibilita la transmisión de voz y datos entre diferentes dispositivos mediante un enlace por radiofrecuencia en la banda ISM de los 2.4 GHz. Los principales objetivos que se pretenden conseguir con esta norma son:
  - Facilitar las comunicaciones entre equipos móviles.
  - Eliminar los cables y conectores entre estos. 
  - Ofrecer la posibilidad de crear pequeñas redes inalámbricas y facilitar la sincronización de datos entre equipos personales.
  
* **Caso sospechoso:** Se considerará a una persona caso sospechoso cuando presente los síntomas habituales y más característicos asociados a la enfermedad.
  
* **Caso sospechoso (COVID-19):** Cuadro clínico de infección respiratoria aguda de aparición súbita de cualquier gravedad que cursa, entre otros, con fiebre, tos o sensación de falta de aire, y que pueden estar asociados o no a síntomas graves como dificultad respiratoria o neumonía. Otros síntomas atípicos como la odinofagia (dolor de garganta al ingerir), anosmia (pérdida de olfato), ageusia (pérdida de gusto), dolores musculares, diarreas, dolor torácico o cefaleas, entre otros, pueden ser también considerados como síntomas de sospecha de infección de Covid-19.

* **Contacto estrecho:** Persona que haya tenido una exposición a la enfermedad de forma que las posibilidades de contagio sean altas y por tanto se le deban hacer las pruebas pertinentes y mantener bajo observación.

* **Contacto estrecho (COVID-19):** Persona que haya coincidido con un caso diagnosticado como COVID positivo, permaneciendo a menos de 2 metros, durante más de 15 minutos, sin mascarilla y durante las 48 horas previas a la fecha del diagnóstico. Si todas las personas usaron mascarillas en todo momento, se mantuvo la distancia de seguridad y el espacio estuvo ventilado no se considerarían contactos estrechos. 

* **Contagio:** Transmisión de una enfermedad por contacto con el agente patógeno que la causa. (El coronavirus tiene un alcance de reproducción de 2,68 según la revista científica Lancet. Es decir, cada persona contagiada llega a contagiar a 2,68 personas, un índice relativamente alto, lo que ha facilitado su expansión por el mundo.)

<img align="right" width=54% src="./Imágenes/covid19.jpeg">

* **Coronavirus:** Gran familia de virus que pueden provocar enfermedades tanto a animales como a humanos. Se sabe que, en los humanos, todos los virus de esta familia pueden causar infecciones respiratorias, que pueden ir desde un resfriado normal a una enfermedad grave, como son la SRAS, la MERS o el Covid-19. La primera vez que se habló de este tipo de virus fue en la revista Nature el 16 de noviembre de 1968. Los investigadores lo llamaron 'coronavirus' porque la forma del virus al microscopio era como similar al de la corona solar como podemos observar en la imagen.

* **COVID-19:** Enfermedad infecciosa causada por el coronavirus SARS-CoV-2 y que se ha descubierto recientemente. El origen léxico del Covid-19 proviene de 'co', en alusión a la forma de corona solar del virus, 'vi' que corresponde a la palabra virus y 'd' que hace referencia a enfermedad ("disease" en inglés). Finalmente se le puso el número 19 por el año en que se detectó en seres humanos.

* **Cuarentena:** Se trata de un aislamiento preventivo durante un tiempo determinado con el objetivo de evitar el contagio de ciertas enfermedades. Lo llevan a cabo personas que están en su domicilio porque poseen confirmación médica de haber contraído una enfermedad o porque están esperando un diagnóstico definitivo (en el caso del Covid-19, a la espera de PCR/test rápido por ser un caso sospechoso o ser un contacto estrecho). No tienen por qué ser 40 días exactos. De hecho, para el caso del Covid-19 suele rondar los 10 días. 

* **Estado de alarma:** En España se declara en todo el país (o en parte de este) mediante un decreto del consejo de ministros en el caso de calamidades, desgracias públicas como inundaciones, terremotos o crisis sanitarias como la que vivimos por culpa del coronavirus. Esta disposición permite limitar la libre circulación de las personas, intervenir industrias, requisar temporalmente bienes, y limitar o racionar los servicios o el consumo de artículos de primera necesidad. Además, permitiría realizar los cambios legales que fueran necesarios para poder obtener los datos de localización de los teléfonos móviles que poseen las diferentes operadoras, e incluso de los fabricantes de teléfonos y sistemas operativos (Google, Apple, etc.).

* **Incubación:** Se trata del tiempo comprendido entre la exposición a un organismo patogénico y el momento en que los síntomas aparecen por primera vez. En el caso del coronavirus, el tiempo de incubación es de 5,4 días de media, aunque se han observado casos en que el periodo de incubación es de hasta 14 días.


<img align="right" width=10% src="./Imágenes/OMS_logo.png">


* **Organización Mundial de la Salud (OMS):** Organismo especializado de las Naciones Unidas creado en 1946 con el propósito fundamental de alcanzar para todos los pueblos el grado más alto posible de salud. Coordina programas encaminados a solucionar problemas sanitarios y se ocupa de la inmunización, la educación sanitaria y el suministro de medicamentos esenciales.

* **Pandemia:** Tal y como establece la OMS, se llama pandemia a la propagación a gran velocidad y a escala mundial de una nueva enfermedad. Lo que la diferencia de la epidemia es el grado en que aumentan los casos y su alcance internacional. La OMS declaró al Covid-19 como pandemia el 11 de marzo de 2020 cuando se extendió por los seis continentes y se certificaron contagios en más de 100 países de todo el planeta.

<img align="right" width=50% src="./Imágenes/PCR7.jpg">

* **PCR:** La reacción en cadena de la polimerasa, conocida como PCR por sus siglas en inglés (polymerase chain reaction), es una técnica de la biología molecular desarrollada en 1986 por Kary Mullis. Su objetivo es obtener un gran número de copias de un fragmento de ADN particular, partiendo de un mínimo; en teoría basta partir de una sola copia de ese fragmento original, o molde. En algunos casos, como en la actual epidemia de coronavirus SARS-CoV-2, se están empleando las PCR para detectar, confirmar o descartar la presencia del coronavirus en el organismo ya que esta prueba de diagnóstico permite localizar y amplificar un fragmento del material genético de un patógeno o microorganismo, que en el caso del coronavirus es una molécula de ARN. El Ministerio de Sanidad subraya en el documento de Estrategia de detección precoz, vigilancia y control del Covid-19 que las muestras recomendadas para la PCR son del tracto respiratorio superior e inferior:
  - Superior: exudado preferiblemente nasofaríngeo y orofaríngeo o exudado nasofaríngeo. 
  - Inferior: preferiblemente lavado broncoalveolar, broncoaspirado, esputo (si es posible) y/o aspirado endotraqueal, especialmente en pacientes con enfermedad respiratoria grave. 
  
  Así, la toma de la muestra se obtiene inclinando ligeramente la cabeza del paciente hacia atrás, se introduce un hisopo o bastoncillo en la garganta, hasta la faringe, y se rota o da vueltas de cinco a 10 segundos, aunque también se puede tomar la muestra del interior de la nariz, por lo que se introduce el bastoncillo por un orificio nasal unos cinco o siete centímetros hasta la nasofaringe y se gira durante unos segundos para obtener el tejido necesario.
  
  En el siguiente enlace se puede ver cómo se debe realizar una PCR: [Link](https://www.youtube.com/watch?v=Yf-HDkJGW08 "¿Cómo se realiza una prueba PCR?").

<img align="right" width=30% src="./Imágenes/test-rapido.png">

* **Test rápido:** Este nuevo test rápido de antígenos es una nueva prueba de la que disponemos que nos permite detectar el Covid-19 desde el mismo inicio del contacto con una altísima fiabilidad, muy similar a la que nos ofrecerá una PCR, pero con obtención de resultados en apenas 15 minutos. Los test rápidos se realizan con muestras de exudados de la nariz y del fondo de la garganta –que se toman con un bastoncillo o hisopo– y en ellos se detectan la posible presencia de antígenos, es decir, permiten detectar si hay presencia del virus SARS-CoV-2 en el paciente por medio de alguno de sus componentes, como por ejemplo, por sus proteínas.

<br>

> En la siguiente imagen podemos ver las principales diferencias entre la técnica de la PCR y los test rápidos en el diagnóstico del Covid-19:

<br><br>
<p align="center">
  <img width=70% src="./Imágenes/diferencia_PCR7_test_rapido.jpg">
</p>


* **Vacuna:** Se trata de una sustancia compuesta por microorganismos atenuados o muertos que se introduce para estimular la formación de anticuerpos y conseguir inmunidad frente a ciertas enfermedades. Hasta la fecha no existe ninguna vacuna ni medicamento antiviral específico para prevenir o tratar el COVID-19.

<br>
<br>

# 3 DESCRIPCIÓN DE LA SITUACIÓN ACTUAL 

El Gobierno de España decidió comenzar a utilizar la aplicación Radar Covid a nivel nacional como parte de las principales soluciones para frenar la pandemia ya que en otros países de la Unión Europea había tenido bastante éxito. Para usar Radar Covid en cada comunidad autónoma, cada una de ellas debía comunicar al Ministerio de Sanidad su uso, y tras comprobar que todo estaba en orden, pedía a la Secretaría de Estado de Inteligencia Artificial (dependiente del Ministerio de Asuntos Económicos y Transformación Digital) que comenzara la integración técnica. Para esta integración técnica, cada comunidad autónoma debía crear un protocolo propio dentro de sus sistemas sanitarios para enviar los códigos a los contagiados (que identifican anónimamente a los casos positivos y permiten informar a sus contactos estrechos sin desvelar la identidad de los casos positivos) y formar a los rastreadores para que pudieran utilizar de la mejor manera posible la información que reciben de la aplicación. Sin embargo, todo este proceso de puesta en marcha fue bastante lento ya que intervinieron gran cantidad de actores. 

Hoy en día, Radar Covid ya se está usando a nivel nacional pero no se están consiguiendo los resultados que se esperaban por diversos motivos como son:
  * El número de descargas de la aplicación es muy bajo ya que es una aplicación de uso voluntario y además se le ha dado poca publicidad en los medios nacionales.
  * A nivel de la población el conocimiento de la tecnología médica en España es insuficiente.
  * La dificultad para comunicar un positivo. Esto se debe a que los sanitarios deben proporcionar a los usuarios diagnosticados como positivos un código para insertar en la aplicación, y sin embargo muchos sanitarios desconocen la existencia de estos códigos. Además, la colaboración por parte de las Comunidades Autónomas no está siendo la adecuada, y surgen continuamente problemas en la generación de códigos ya que la gestión de los datos entre las diferentes comunidades no está estandarizada.
  * Está basada en el uso de Bluetooth, lo que la hace inservible si el Bluetooth está apagado o bien, ocupado con los auriculares u otra aplicación.
  
  
  Como apenas se está utilizando esta aplicación, los sanitarios y rastreadores deben rastrear de forma manual los contactos estrechos de cada paciente que es diagnosticado como positivo. Todo esto supone una gran pérdida de tiempo porque si Radar Covid estuviera funcionando en todos los dispositvos móviles se podría automatizar este proceso.  Además, como este rastreo se hace de forma manual, es necesario crear también de forma manual las citas médicas para las personas que deban acudir a realizarse las pertinentes pruebas médicas.
  
  Cabe destacar el hecho de que actualmente si una persona no acude a realizarse las pruebas médicas, son los sanitarios los encargados de llamar a la persona para comprobar porque no ha acudido y en numerosas ocasiones no los localizan, pero en ningún momento se avisa a las fuerzas del orden para que vayan a ver que sucede. 
  
  Finalmente, todas las personas que se realizan test rápidos o PCR deben guardar una cuarentena de aproximadamente 10 días hasta que vuelvan a dar negativo en una segunda PCR, y son los propios sanitarios los encargados de comprobar que las personas están realizando la cuarentena. Este proceso se realiza llamando a cada una de las personas por teléfono pero debido a que el número de personas que deben realizar las cuarentenas cada vez es mayor, se intenta llamar a todos varias veces pero con preferencia sobre los casos positivos.
  
Por todo ello y más, nace Pandemio, que tratará de rastrear y gestionar la información de los ciudadanos de la próxima pandemia de una forma más eficaz y eficiente.
Para ello es necesario conocer en detalle la situación actual para evitar cometer los mismos errores de Radar Covid en Pandemio y mejorar lo que ya es positivo.

<br>

## 3.1 Pros y contras de la Situación Actual
En esta sección señalaremos los principales aspectos positivos y negativos de la situación actual para que no sucedan en el futuro, y aquellos relacionados con Radar Covid con el fin de conservar sus fortalezas, pero corrigiendo las debilidades que la han llevado a fracasar para que no suceda lo mismo con Pandemio. De esta forma se podrá automatizar la mayoría de los procesos, y conseguir una mejor gestión de una futura pandemia y un menor impacto en la población:

### 3.1.1 Fortalezas de la Situación Actual
Los principales aspectos positivos que podemos destacar de la situación actual son las siguientes:


| **ID** | **NOMBRE** | **DESCRIPCIÓN** |
| :-----: | :----- | :----- |
| **FO_01** | Acceso a móviles | Actualmente la mayoría de la población tiene teléfono móvil con GPS y acceso a internet, lo que facilita la implementación de estas aplicaciones software para controlar la pandemia. |
| **FO_02** | Sistema sanitario | En España contamos con cobertura sanitaria universal y un sistema de salud muy competente. |
| **FO_03** | Conciencia social | La mayor parte de la gente está concienciada de la situación actual y trata de cumplir las medidas sanitarias que se imponen para reducir el impacto del virus en la población. |
| **FO_04** | Conocimiento de procedimientos | Tanto el personal sanitario como la mayoría de la población están familiarizados con los pasos a seguir en cualquier situación relacionada con la pandemia, casos sospechosos, contactos estrechos, casos positivos... |
| **FO_05** | Conocimiento del virus | Nuestro conocimiento actual del virus es mayor que al comienzo de la pandemia. |
| **FO_06** | Aplicaciones software | Han aparecido numerosas aplicaciones que tratan de combatir la expansión del Covid-19 como Radar Covid. En concreto, esta aplicación tiene numerosos aspectos buenos a destacar como el anonimato o la descentralización de los datos (los detallaremos a continuación), aunque no haya tenido gran impacto en la sociedad española. |



Algunos de los aspectos positivos que posee Radar Covid y que convendría mantenerlos en Pandemio para una mejor gestión de una futura pandemia son:
| **ID** | **NOMBRE** | **DESCRIPCIÓN** |
| :-----: | :----- | :----- |
| **FO_06.1** | Anonimato | La aplicación funciona sin revelar la identidad del usuario ni la del teléfono móvil. Además, no registra datos personales ni de geolocalización. |
| **FO_06.2** | Alertas rápidas | Rápido aviso al usuario de que ha estado en contacto con un positivo cercano para que comience la cuarentena cuanto antes y disminuya sus contactos sociales. |
| **FO_06.3** | Discreción | Las alertas de exposición se envían sin indicar el lugar ni momento concreto donde se produjo la exposición. |
| **FO_06.4** | Descentralización de los datos | Los datos de cada usuario solo se guardan en su teléfono móvil. |
| **FO_06.5** | Encriptación de los datos | La conexión entre los teléfonos móviles y el servidor es privada. |
| **FO_06.6** | Interfaz amigable | Fácil uso de la interfaz. |
| **FO_06.7** | Sección de ayuda | Tiene sección de preguntas y enlaces de interés acerca de la enfermedad. |
| **FO_06.8** | Varios idiomas | Posibilidad de usar la aplicación en varios dialectos (catalán, euskera, gallego y valenciano) e idiomas (español e inglés). |
| **FO_06.9** | Gratuita | Es gratuita y fácilmente instalable. |
| **FO_06.10** | Anonimato | Es posible comunicar de forma anónima el diagnostico positivo de una prueba PCR o un test rápido. |
| **FO_06.11** | Consumo de datos nulo | No consume ningún dato de las tarifas telefónicas. |
| **FO_06.12** | Código abierto | El código fuente de la aplicación de rastreo está publicado en GitHub para que cualquier desarrollador externo pueda notificar errores y colaborar. |
 


### 3.1.2 Debilidades de la Situación Actual

Por el contrario, las principales debilidades de la situación actual son las siguientes:

| **ID** | **NOMBRE** | **DESCRIPCIÓN** |
| :---: | :----- | :----- |
| **DE_01** | Presencia de asintomáticos | Hay muchas personas que son asintomáticas. Estas personas son contagiadoras a pesar de no presentar síntomas y son muy difíciles de detectar por esa misma razón. |
| **DE_02** | Negacionistas | Existencia de un grupo de población que niega la existencia del virus y por tanto se niega a acatar toda norma de conducta social para evitar/reducir contagios. |
| **DE_03** | Incumplimiento de las normas | Hay parte de la población que incumple o trata de incumplir las normas siempre que puede por falta de concienciación o de responsabilidad individual. |
| **DE_04** | Falsos negativos en pruebas | Un resultado negativo en la primera prueba PCR puede llevar a la persona a no hacer cuarentena (a pesar de estar informada por los sanitarios), y en caso de ser un falso negativo esto podría producir nuevos contagios. |
| **DE_05** | Comprobación cuarentena | Actualmente los sanitarios llevan solo el seguimiento de la cuarentena de los casos positivos y negativos por teléfono cada 2-3 días, sin posibilidad de confirmar la ubicación de la persona de ninguna manera. |
| **DE_06** | Asistencia "voluntaria" | En caso de que una persona no acuda a realizarse las oportunas pruebas médicas, los sanitarios solo pueden tratar de ponerse en contacto por teléfono con la persona y en numerosas ocasiones no responden. En ningún momento se pide ayuda a las fuerzas del orden. |
| **DE_07** | Rastreo de personas sin móvil | No toda la población utiliza teléfonos móviles, por lo cual el rastreo a estas personas debe ser realizado a través de personas cercanas a ellos, lo cual puede conllevar cierto descontrol y pérdida de información. |
| **DE_08** | Cierre de negocios | La mala gestión de esta pandemia ha provocado el cierre de numerosos negocios y un desplome de la economía. |
| **DE_09** | Medidas por CCAA | Cada CCAA adopta sus propias medidas en la lucha contra la pandemia lo que dificulta que las personas sepan realmente las que se adoptan en su CCAA o en las CCAA a las que se desplazan. |
| **DE_10** | Comunicación entre CCAA | El hecho de que la sanidad esté transferida hace que tengamos que hacer un esfuerzo especial para notificar los casos positivos desplazados y mantener una comunicación fluida entre comunidades. |
| **DE_11** | Rastreo en zonas rurales | Debido a la dificultad de rastreo en zonas rurales a través de la triangulación de antenas móviles por la falta de éstas, se necesitará en estos casos que su GPS permanezca activado. |
| **DE_12** | Aplicación software | La aplicación Radar Covid que se está utilizando a nivel nacional para la gestión de la pandemia tiene muchos inconvenientes (los detallaremos a continuación) y apenas ayuda al rastreo del virus. |



Algunos aspectos negativos que tiene la aplicación de Radar Covid y que provocan que no sea efectiva en la lucha contra esta pandemia son los que se detallan a continuación. Si todos estos aspectos negativos se mejoraran en Pandemio, se podría lograr un mejor rastreo del virus y gestión de la información:

| **ID** | **NOMBRE** | **DESCRIPCIÓN** |
| :---: | :----- | :----- |
| **DE_12.1** | Descarga y uso voluntario | La instalación y el uso de la aplicación no son obligatorios lo que dificulta el rastreo del virus en la población ya que solo un pequeño porcentaje de la población la usa diariamente. |
| **DE_12.2** | Sanitarios poco familiarizados con la App | No todo el personal sanitario está familiarizado con el funcionamiento de la aplicación y muy pocos hacen uso de ella. |
| **DE_12.3** | Desconocimiento de la App | Gran parte de la población no conoce la existencia de la aplicación. |
| **DE_12.4** | Vulnerabilidad a ataques | El uso del Bluetooth provoca que los teléfonos móviles sean más vulnerables a ataques informáticos. |
| **DE_12.5** | Funcionamiento basado en Bluetooth y GPS | La aplicación hace uso del Bluetooth para su correcto funcionamiento y generalmente suele estar apagado u ocupado por otros dispositivos. Esto provoca que las aplicaciones actuales no funcionen correctamente y que el rastreo del virus sea aún más complicado. Además, hay teléfonos móviles que aún no tienen buenos servicios de GPS incorporados. |
| **DE_12.6** | Incompatibilidad entre Apps | El uso del Bluetooth en varias aplicaciones puede generar problemas de incompatibilidad entre ellas y que los sistemas software no funcionen correctamente. |
| **DE_12.7** | Desconocimiento del Bluetooth | Mucha gente mayor no conoce cómo funciona el Bluetooth por lo que las aplicaciones que se basan en Bluetooth pierden su potencial. |
| **DE_12.8** | Desconocimiento del propio teléfono móvil | Mucha gente de avanzada edad desconoce cómo usar los teléfonos móviles y como descargar aplicaciones. |
| **DE_12.9** | Nula estandarización | Las bases de datos de las diferentes administraciones no están estandarizadas lo que provoca que muchos usuarios no puedan informar de su resultado positivo si se mueven entre distintas comunidades. |


<br>

## 3.2	Modelos de Procesos de Negocio Actuales

En la lucha contra el Covid-19 intervienen gran cantidad de actores ya que cada uno tiene su función para evitar reducir el impacto de la pandemia en la población. Hay que destacar el trabajo de los sanitarios, rastreadores y fuerzas del orden que se encuentran en primera línea en esta lucha contra el virus. Para conseguirlo, se llevan a cabo varios procesos como son la realización de pruebas médicas o el rastreo de contactos estrechos que se detallan más adelante.


### 3.2.1 Descripción de los Actores de Negocio Actuales

Los principales actores de negocio que intervienen en la actualidad en la lucha contra el Covid-19 son: 

| **ID** | **Nombre** | **Descripción** |
| :---: | :--- | :--- |
| **AC_01** | Gobierno de España | Es el órgano que se encarga de decidir en última instancia el confinamiento domiciliario de una localidad o del país. Además, se encargó de que Radar Covid se comenzará a utilizar en España así como de permitir e impulsar su uso. |
| **AC_02** | Secretaría de Estado de Digitalización e Inteligencia Artificial del Gobierno de España | Esta secretaría, dependiente del Ministerio de Asuntos Económicos y Transformación Digital, es la encargada de personalizar la aplicación de Radar Covid para España (ya que es una aplicación que se usa en toda Europa y tiene su origen fuera de España) e integrarla en los servicios sanitarios de cada comunidad autónoma. Además, es la encargada de impulsar la aplicación en España y subsanar cualquier brecha de seguridad que pudiera surgir. |
| **AC_03** | Sanidad de cada CCAA | Actualmente la Sanidad de España está transferida, por lo que cada comunidad autónoma debe decidir sus protocolos a seguir cuando el número de contagios crece, aunque en algunas ocasiones debe pedir la aprobación del Gobierno de España. Además se encarga de crear los protocolos de Radar Covid dentro de cada comunidad autónoma, de formar a los sanitarios y a los rastreadores, y comunicarse con otras comunidades autónomas cuando existen casos que se mueven entre distintas comunidades autónomas. |
| **AC_04** | Sanitarios y rastreadores | Son los encargados de generar los códigos para los ciudadanos que hayan obtenido un resultado positivo ya que los usuarios que usan la aplicación no los pueden generar por sí mismos. Además, son los encargados de rastrear el virus y los posibles contactos estrechos que hayan mantenido los ciudadanos con una persona con diagnóstico positivo. También se encargan de comprobar si está realizando la cuarentena o no. |
| **AC_05** | Fuerzas del orden | Son los encargados de que se cumplan las normas impuestas por cada CCAA o por el Gobierno y de multar a aquellos que las incumplan. También se encargan de controlar la circulación de los ciudadanos cuando existen restricciones de movilidad.  |
| **AC_06** | Usuarios de la app Radar Covid | Debido a que Radar Covid es una aplicación de uso voluntario, es necesario que los ciudadanos se descarguen esta aplicación y la usen correctamente. Deben usar el Bluetooth y el GPS, y son los encargados de comunicar su positivo a través de la aplicación cuando han obtenido un diagnóstico médico positivo para lograr un mejor rastreo del virus en la población. |


### 3.2.2 Descripción de Procesos de Negocio Actuales

Para el rastreo y gestión de la pandemia Covid se llevan a cabo los siguientes procesos:

| **PR_01** | **Realizar pruebas médicas** |
| :---: | :--- |
| **Descripción** | Cuando una persona es considerada contacto estrecho se le asignará una cita médica. Cuando acude a la cita médica, si presenta síntomas se le realiza un test rápido y si el resultado es positivo se confirma que la persona tiene COVID-19, en caso de resultado negativo se realizará una prueba PCR para confirmarlo. Si no tiene síntomas se le realiza directamente una prueba PCR. A continuación, se seguirán los procesos oportunos dependiendo si los resultados de las pruebas médicas han sido negativos o positivos. |

En el siguiente diagrama de actividad podemos ver un resumen de este proceso:

<p align="center">
<img width=50% src="./Imágenes/Realizar_pruebas_médicas.jpg">
</p>

<br>

| **PR_02** | **Asignar código** |
| :---: | :--- |
| **Descripción** | Después de que un paciente haya acudido a realizarse una prueba médica, los sanitarios comprueban el resultado. Si el resultado de la prueba es positivo, tienen que solicitar al sistema un código que el paciente podrá introducir voluntariamente en la aplicación Radar Covid. |

En el siguiente diagrama de actividad podemos ver un resumen de este proceso:

<p align="center">
<img width=40% src="./Imágenes/Asignar_codigo.jpg">
</p>

<br>

| **PR_03** | **Establecer cuarentena y seguimiento** |
| :---: | :--- |
| **Descripción** | Tras realizarse las pruebas médicas, independientemente de que el resultado sea positivo o negativo, la persona deberá cumplir un periodo de cuarentena de aproximadamente 10 días. Entre el séptimo y el décimo se realizará una segunda prueba PCR que determinará, en caso de positivo, una ampliación de la cuarentena y, en caso de negativo, se dará el alta médica y la persona podrá hacer vida normal. Actualmente los sanitarios llevan el seguimiento por teléfono de la cuarentena de todos los casos confinados (haciendo incapié en los positivos) cada 2-3 días, aunque no pueden confirmar de ninguna forma la ubicación de la persona. |

En el siguiente diagrama de actividad podemos ver un resumen de este proceso:

<p align="center">
<img width=50% src="./Imágenes/Establecer_cuarentena_y_seguimiento.jpg">
</p>

<br>

| **PR_04** | **Rastrear contactos** |
| :---: | :--- |
| **Descripción** | Cuando una persona da positivo los sanitarios deben rastrear los contactos estrechos de esta persona, para ello preguntarán al paciente con quién ha estado los dos días antes de tener síntomas Covid. Una vez recogidos estos datos, los sanitarios llaman de forma individual a cada uno de estos contactos y conciertan citas para realizar las pruebas médicas siguiendo el procedimiento PR_01. En caso de que un caso confirmado positivo se haya desplazado o haya estado en otra comunidad autónoma dos días antes de conocer que ha sido positivo, se avisará al cuerpo sanitario de dicha comunidad para que realicen el rastreo y las pruebas médicas oportunas.  |

En el siguiente diagrama de actividad podemos ver un resumen de este proceso:

<p align="center">
<img width=60% src="./Imágenes/Rastrear_contactos.jpg">
</p>

<br>


| **PR_05** | **Comprobar medidas sanitarias** |
| :---: | :--- |
| **Descripción** | Diariamente las autoridades sanitarias de cada CCAA revisan la incidencia de la pandemia en la población, y en función de los datos obtenidos se toman diferentes medidas como pueden ser el cierre perimetral de la localidad, cierre de la hostelería, limitación de movimiento entre provincias/CCAA, confinamiento domiciliario. |

En el siguiente diagrama de actividad podemos ver un resumen de este proceso:

<p align="center">
<img width=25% src="./Imágenes/Comprobar_medidas_sanitarias.jpg">
</p>


<br>

## 3.3 ENTORNO TECNOLÓGICO ACTUAL

Cada CCAA utiliza una aplicación software propia donde los sanitarios y los rastreadores registran todos los datos médicos y las pruebas médicas que se realiza cada persona a lo largo de su vida. Por poner algún ejemplo de aplicación destacamos Medora que es la que se usa en Castilla y León.

Por otro lado, para combatir la actual pandemia de Covid-19, se usan algunas aplicaciones móviles como CoronaMadrid (en Madrid) o COVID-19.eus (en el País Vasco). La mayoría usan un sistema similar a Radar Covid que es la aplicación que se usa a nivel nacional y que detallaremos a continuación.

Radar Covid es una aplicación de código abierto que podemos encontrar en el siguiente link: [https://github.com/RadarCOVID](https://github.com/RadarCOVID) y utiliza el protocolo abierto 'Decentralized Privacy-Preserving Proximity Tracing' (DP-3T, estilizado como dp3t), que fue desarrollado en respuesta a la pandemia Covid-19 para facilitar el rastreo de contactos digitales de los participantes infectados. 

Cuando dos usuarios que tienen Radar Covid activado se encuentran, si permanecen juntos durante un tiempo superior a 15 minutos, sus teléfonos móviles intercambian los números identificadores de la aplicación y los almacenan localmente en sus registros de contacto. 

Cuando uno de ellos obtiene un resultado positivo en un análisis médico, si introduce un código en la aplicación (este código se lo proporcionan los sanitarios), se envía un informe a un servidor central informando de su caso de manera anónima. 

Continuamente la aplicación recopila los informes del servidor de forma automática y comprueba si algún identificador contenido en el informe del servidor se encuentra entre sus registros de contacto locales. Si encuentra alguna coincidencia, entonces el usuario ha estado en contacto cercano con un paciente diagnosticado como positivo, y es advertido por la aplicación. Puesto que cada dispositivo verifica localmente los registros de contacto, y por lo tanto los registros de contacto nunca se transmiten a terceros, el servidor de informes central no puede por sí mismo determinar la identidad o el registro de contacto de cualquier usuario de la aplicación.

El protocolo de enlace del dispositivo utiliza Bluetooth Low Energy para encontrar e intercambiar detalles entre los usuarios de la aplicación que se encuentren en un rango cercano, y la fase de notificación de infecciones utiliza HTTPS para cargar el informe en un servidor central de Amazon Web Services.

Finalmente, el código fuente de la aplicación está escrito en su mayoría en Kotlin (lenguaje de programación con tipo estático desarrollado por JetBrains y que se utiliza con mayor frecuencia para complementar o reemplazar Java en aplicaciones empresariales y de usuario final) y XML para la parte de cliente, y Java para la parte de servidor, y utiliza SQL para realizar las búsquedas en las bases de datos. 


### 3.3.1 Descripción del Entorno de Hardware Actual

Por un lado destacan los ordenadores de los centros de salud y hospitales con los que los sanitarios gestionan los historiales clínicos de cada persona. Además cada CCAA tiene sus propias bases de datos y se encargan de su gestión ya que la Sanidad está transferida.

Por otro lado se encuentra el entorno hardware de la aplicación Radar Covid que consiste en los teléfonos móviles de cada usuario, en los servidores de Amazon Web Services y en los ordenadores de los centros de salud y hospitales que generan los códigos que los contactos positivos pueden introducir voluntariamente en la aplicación. 

Además, también podemos destacar los ordenadores del Gobierno de España, concretamente los de la Secretaría de Estado de Inteligencia Artificial, encargados del mantenimiento y buen funcionamiento de la aplicación de Radar Covid en todo momento. 

### 3.3.2 Descripción del Entorno de Software Actual

Como ya se dijo antes, cada CCAA utiliza su propia aplicación software (como Medora en CyL) para gestionar las historias clínicas de cada persona. También se utilizan aplicaciones móviles en algunas comunidades autónomas como Madrid o País Vasco para combatir el Covid-19, pero la única aplicación que se usa a nivel nacional con este objetivo es Radar Covid.

El entorno software de Radar Covid es bastante simple a nivel de usuario final ya que se trata de una aplicación móvil disponible en Android e iOS y para su correcto funcionamiento solo es necesario el uso del Bluetooth y del GPS. 

La gestión de los datos de Radar Covid está basada en el modelo descentralizado ya que los datos de cada usuario se guardan en cada teléfono móvil. Los pocos datos que se comparten con la aplicación están alojados en los servidores de Amazon Web Services y la subida de datos al servidor se hace con un software de la compañía estadounidense de forma cifrada y anónima para guardar la confidencialidad y el anonimato de los usuarios de la aplicación.

Finalmente también es necesario un programa generador de códigos que utiliza el personal sanitario cuando un ciudadano obtiene un resultado positivo en un test rápido o en una PCR. Este código generado es el que se le da al ciudadano para que lo registre voluntariamente en su aplicación de Radar Covid y se avise a todas las personas que hayan estado más de 15 minutos con él.

 <br>
 <br>
 
 # 4 NECESIDADES DE NEGOCIO

Dado que la actual pandemia provocada por el Covid-19 está dejando datos muy preocupantes: un gran número de contagiados y de muertes, las UCIs por encima de su capacidad máxima, un gran número de operaciones pospuestas por falta de espacios en los hospitales, etc. y las aplicaciones que existen actualmente como Radar Covid no terminan de ayudar en la lucha para frenar la expansión del Covid-19, es necesario crear una nueva aplicación software que mejore la anterior y que ayude a reducir el impacto de una futura pandemia en la sociedad, ya que una mala gestión en una pandemia más grave podría ser catastrófica. 

<br>

## 4.1 Objetivos de Negocio

En la siguiente tabla se describen los principales objetivos que se esperan alcanzar con Pandemio cuando se termine de implementar:
 
 | **OB_01** | Mejorar las aplicaciones software existentes en la lucha contra una futura pandemia. | 
 | :--: | :----- |
 | **Descripción** | El sistema software existente en España no ha funcionado como se esperaba y se tratará de mejorar para reducir el impacto de una futura pandemia. |
 | **Subobjetivos** | - Automatizar los procesos de negocio actuales.|
 | **Importancia** | Alta. |
 | **Prioridad** | Media. |
 
 | **OB_02** | Alcanzar el 100% de la población que disponga de teléfonos móviles. | 
 | :--: | :----- |
 | **Descripción** | El sistema software intentará llegar al 100% de la población para tener control total sobre los casos y los contagios. |
 | **Subobjetivos** | - Lograr la instalación obligatoria de la aplicación de Pandemio en todos los teléfonos móviles. <br> - Obligar a usar la aplicación a turistas que vengan a España. |
 | **Importancia** | Alta. |
 | **Prioridad** | Alta. |
 
 | **OB_03** | Alcanzar el mayor número de población posible. | 
 | :--: | :----- |
 | **Descripción** | Dado que una pequeña parte de la población vive en los pueblos y puede no tener acceso a un teléfono móvil se deberá realizar un esfuerzo especial para tenerlos controlados. |
 | **Subobjetivos** | - Crear campañas publicitarias para fomentar el aviso de positivos de personas sin acceso a teléfonos móviles. <br> - Permitir el aviso de casos sospechosos/positivos de personas que no dispongan de teléfono móvil mediante un formulario desde el teléfono móvil de las personas que dependan. <br> - Permitir el uso de la aplicación en distintos dialectos/idiomas (catalán, gallego, euskera, valenciano e inglés).   |
 | **Importancia** | Alta. |
 | **Prioridad** | Media. |
 
 | **OB_04** | Rastrear y gestionar la información de los usuarios de forma anónima. | 
 | :--: | :----- |
 | **Descripción** | Gestión de la información de forma anónima respetando la ley de protección de datos. |
 | **Subobjetivos** | - Almacenar los datos de los usuarios de forma anónima. <br> - Compartir solo los datos esenciales con el personal sanitario y/o fuerzas del orden. |
 | **Importancia** | Alta. |
 | **Prioridad** | Media. |
 
 | **OB_05** | Preservar la privacidad de los usuarios. | 
 | :--: | :----- |
 | **Descripción** | Aplicación de la ley de protección de datos. |
 | **Subobjetivos** | - Restringir el acceso a los datos a usuarios sin identificar. <br> - Obtener un listado de los datos a los que ha accedido cada usuario. |
 | **Importancia** | Media. |
 | **Prioridad** | Media. |
 
 | **OB_06** | Reducir el impacto de futuras pandemias en la sociedad. | 
 | :--: | :----- |
 | **Descripción** | Reducción del impacto que está teniendo la pandemia actual, principalmente en términos de salud y economía, y estar preparados para futuras pandemias.  |
 | **Subobjetivos** | - Reducir la mortalidad. <br> - Reducir el número de contagios. <br> - Reducir el impacto en la economía. |
 | **Importancia** | Alta. |
 | **Prioridad** | Media. |
 
 | **OB_07** | Automatizar el proceso de citaciones para realizar pruebas médicas. | 
 | :--: | :----- |
 | **Descripción** | Automatización de las citaciones médicas. |
 | **Subobjetivos** | - Generar una cita médica al validar los formularios recibidos. <br> - Generar una cita médica si un usuario ha estado cerca de un caso positivo.|
 | **Importancia** | Media. |
 | **Prioridad** | Baja. |
 
 | **OB_08** | Informar a los usuarios que deben acudir a realizarse pruebas médicas. | 
 | :--: | :----- |
 | **Descripción** | Notificar a un usuario que tiene que ir a realizarse una prueba médica por haber estado en contacto con un usuario que ha dado positivo o por informar de síntomas característicos de la enfermedad. |
 | **Subobjetivos** | - Generar notificaciones automáticas. <br> - Generar notificaciones que no se puedan eliminar del menú de notificaciones de los teléfonos móviles. |
 | **Importancia** | Media. |
 | **Prioridad** | Media. |
 
 | **OB_09** | Avisar a las fuerzas del orden si un usuario no acude a realizarse las pruebas médicas. | 
 | :--: | :----- |
 | **Descripción** | Notificar a las fuerzas del orden si un usuario no se realiza las pruebas médicas pertinentes cuando tenga una cita médica asignada. |
 | **Subobjetivos** | - Automatizar el proceso de notificación a las autoridades para estos casos. |
 | **Importancia** | Media. |
 | **Prioridad** | Baja. |
 
 | **OB_10** | Avisar a las fuerzas del orden si un usuario no cumple con la cuarentena que se le ha impuesto. | 
 | :--: | :----- |
 | **Descripción** | Informar a las fuerzas del orden de que no se están cumpliendo las medidas de cuarentena establecidas. |
 | **Subobjetivos** | - Automatizar el proceso de notificación a las autoridades para estos casos.  |
 | **Importancia** | Media. |
 | **Prioridad** | Baja. |
 
 | **OB_11** | Verificar de forma automática que los usuarios cumplen las cuarentenas impuestas. | 
 | :--: | :----- |
 | **Descripción** | Comprobar que los usuarios cumplen la cuarentena obligatoria sin necesidad de hacerlo manualmente. |
 | **Subobjetivos** | - Introducir la verificación por medio de huella dactilar o facial <br>- Realizar llamadas aleatorias a casos positivos para confirmar su posición. |
 | **Importancia** | Media. |
 | **Prioridad** | Media. |
 
 | **OB_12** | Rastrear a los contactos estrechos de los usuarios. | 
 | :--: | :----- |
 | **Descripción** | Obtener los contactos estrechos de personas que hayan sido diagnosticadas como positivas. |
 | **Subobjetivos** | - Obtener listado de los contactos estrechos. <br> - Notificar a los contactos estrechos.   |
 | **Importancia** | Media. | 
 | **Prioridad** | Media. |
 
 | **OB_13** | Mostrar un mapa de calor con las zonas de movilidad de los casos positivos. | 
 | :--: | :----- |
 | **Descripción** | Muestreo de las zonas de movilidad de los casos positivos con un mapa de calor. |
 | **Subobjetivos** | - Almacenar historial de ubicación de usuarios diagnosticados como positivos. <br>- Gestionar los historiales de ubicación. <br>- Actualizar el mapa de calor cuando se detecten nuevos casos positivos. <br>- Actualizar el mapa de calor cuando se dé de alta a una persona diagnosticada como positiva. <br> - Eliminar historial de ubicación de un usuario cuando ya no se considere positivo. <br> - Generar informes para el Gobierno con estadísticas por zonas. |
 | **Importancia** | Baja. |
 | **Prioridad** | Baja. |
 
  | **OB_14** | Coordinación entre CCAA y países | 
 | :--: | :----- |
 | **Descripción** | Comunicación rápida del movimiento entre comunidades o países de personas positivas para la gestión y el rastreo de la enfermedad. |
 | **Subobjetivos** | - Sincronizar los datos de las personas que se desplacen en las diferentes bases de datos de cada CCAA. <br> - Avisar de posibles casos positivos al país correspondiente si una persona considerada contacto estrecho/caso positivo sale del país. |
 | **Importancia** | Alta. |
 | **Prioridad** | Baja. |
 
<br>
 
 ## 4.2 Modelos de Procesos de Negocio a Implantar 

Con el fin de cumplir todos los objetivos expuestos anteriormente, y sobre todo con el fin de reducir el impacto de una posible pandemia en el futuro, se deberán implantar nuevos actores o modificar las tareas que realizan los ya existentes, y crear o cambiar algunos procesos de los que se están siguiendo para la pandemia del Covid-19.


### 4.2.1 Descripción de los Actores de Negocio a Implantar

Los principales actores de negocio que cambiarán sus funciones una vez terminado el proyecto son los siguientes:  

| **ID** | **Nombre** | **Descripción** |
| :---: | :--- | :--- |
| **ACI_01** | Gobierno de España | Es el órgano que se encargará de tomar las decisiones que afecten a todo el país como es la implantación de Pandemio en todos los dispositivos móviles o el confinamiento domiciliario de una localidad o del país. También se encargará de impulsar las nuevas medidas que se tomen y de crear algunos de los protocolos que puedan utilizar las CCAA. |
| **ACI_02** | Secretaría de Estado de Digitalización e Inteligencia Artificial del Gobierno de España | Esta secretaría, dependiente del Ministerio de Asuntos Económicos y Transformación Digital, será la encargada de gestionar todo lo que tenga que ver con la aplicación de Pandemio. Esto incluirá la gestión de la aplicación y la subsanación de cualquier brecha de seguridad que pudiera surgir. |
| **ACI_03** | Sanidad de cada CCAA | Actualmente la Sanidad de España está transferida y en futuro cercano seguirá así, es por ello que se encargará de crear los protocolos sanitarios dentro de cada comunidad autónoma o de asumir aquellos impuestos por el Gobierno, y de formar a los sanitarios y a los rastreadores en la lucha contra la nueva pandemia. |
| **ACI_04** | Sanitarios y rastreadores | Serán los encargados de realizar las pruebas médicas oportunas, y de avisar a las fuerzas del orden si alguien no acude a realizarse dichas pruebas estando citado para ellas. Además, se encargarán de comprobar que aquellas personas que deben guardar cuarentena la están cumpliendo realmente. De no ser así, se encargarán de avisar a las fuerzas del orden para que acudan a ver que sucede. |
| **ACI_05** | Fuerzas del orden | Al igual que ahora, serán los encargados de que se cumplan las normas impuestas por cada CCAA o por el Gobierno y de multar a aquellos que las incumplan. También se encargarán de controlar la circulación de los ciudadanos cuando existan restricciones de movilidad. Finalmente, tendrán que investigar porque una persona no ha asistido a las pruebas médicas oportunas si reciben un aviso de los sanitarios y de comprobar el cumplimiento de la cuarentena de aquellas personas que no dispongan de teléfonos móviles. |
| **ACI_06** | Usuarios de la app Pandemio | Serán los encargados de comunicar casos sospechosos o positivos de familiares que no dispongan de teléfonos móviles como pueden ser niños pequeños, ancianos dependientes, personas discapacitadas, etc. |

Además, debemos destacar la presencia de un nuevo actor de negocio que en la actualidad casi no tiene peso en la lucha contra el Covid-19 pero que deberá asumir más tareas en una futura pandemia a pesar de que la Sanidad este transferida (y en caso de no estarlo, desarrollar todas las funciones de ACI_03):

| **ID** | **Nombre** | **Descripción** |
| :---: | :--- | :--- |
| **ACI_07** | Ministerio de Sanidad | Será el encargado de impulsar el uso de Pandemio por medio de campañas publicitarias para que los usuarios que tengan a su cargo a personas sin teléfonos móviles informen de casos sospechosos o positivos. |


### 4.2.2 Descripción de Procesos de Negocio a Implantar

Para el rastreo y gestión de una futura pandemia se llevarán a cabo los siguientes procesos:

| **PRI_01** | **Realizar pruebas médicas** |
| :---: | :--- |
| **Descripción** | Cuando una persona sea considerada contacto estrecho se le asignará una cita médica automáticamente. Si acude a la cita médica, se seguirán los procesos oportunos dependiendo si los resultados de las pruebas médicas han sido negativos o positivos (dependerá de las pruebas que se realicen) y se establecerá una cuarentena para evitar la expansión de la enfermedad, y en caso de no acudir, se avisará a las fuerzas del orden para que investiguen la causa. |

En el siguiente diagrama de actividad podemos ver un resumen de este proceso:

<p align="center">
<img width=80% src="./Imágenes/Realizar_pruebas_medicas_futuro.jpg">
</p>

<br>

| **PRI_02** | **Establecer cuarentena y seguimiento** |
| :---: | :--- |
| **Descripción** | Independientemente de que el resultado sea positivo o negativo, la persona deberá cumplir un periodo de cuarentena del número de días que se considere necesario. Durante esta cuarentena, se realizará el control de la cuarentena de forma remota en caso de que la persona disponga de teléfono móvil, y en caso de no tenerlo, las fuerzas del orden acudirán a ver si se está cumpliendo. Si al realizar el control de la cuarentena de forma remota se detecta que la persona no la está cumpliendo, se avisar a las fuerzas de orden para que acudan a ver el motivo y sancionar a la persona. |

En el siguiente diagrama de actividad podemos ver un resumen de este proceso:

<p align="center">
<img width=80% src="./Imágenes/Establecer_cuarentena_y_seguimiento_futuro.jpg">
</p>

<br>

| **PRI_03** | **Rastrear contactos** |
| :---: | :--- |
| **Descripción** | En esta ocasión será la aplicación de Pandemio la que se encargue de forma automática del rastreo de los contactos. Para ello comprobará el historial de ubicaciones del usuario y si la aplicación detecta que el usuario ha estado cerca de una persona que ha dado positivo en las pruebas médicas oportunas, avisará al usuario y creará una cita médica automáticamente para que se realice las pruebas médicas oportunas. En caso de personas que se trasladen entre CCAA o países será el propio sistema el encargado de compartir sus datos y realizar el aviso.|

En el siguiente diagrama de actividad podemos ver un resumen de este proceso:

<p align="center">
<img width=40% src="./Imágenes/Rastrear_contactos_futuro.jpg">
</p>

<br>


| **PRI_04** | **Comprobar medidas sanitarias** |
| :---: | :--- |
| **Descripción** | Este proceso es igual al que existe en la actualidad (PR_05): Diariamente las autoridades sanitarias de cada CCAA revisarán la incidencia de la pandemia en la población, y en función de los datos obtenidos se tomarán diferentes medidas como pueden ser el cierre perimetral de la localidad, cierre de la hostelería, limitación de movimiento entre provincias/CCAA, confinamiento domiciliario. |

En el siguiente diagrama de actividad podemos ver un resumen de este proceso:

<p align="center">
<img width=25% src="./Imágenes/Comprobar_medidas_sanitarias.jpg">
</p>


<br>
<br>

# 5. DESCRIPCIÓN DE LOS SUBSISTEMAS DEL SISTEMA A DESARROLLAR 

A continuación, mostramos el árbol de características con las primeras funcionalidades que se esperan de Pandemio tras la primera entrevista realizada al ministro y que iremos completando a medida que avance el proyecto:

<p align="center">
  <img src="./Imágenes/Arbol_de_caracteristicas_v2.0.jpg">
</p>

<br>

Además, en las siguientes tablas se trata de realizar una descripción detallada de los diferentes subsistemas a desarrollar que se observan en el árbol de características de Pandemio. 

|**SUB_01**| **Gestor de localizaciones** |
| :---: | :--- |
|**Dependencias**| Los objetivos de negocio de los que depende son: <br> + OB_02 - Alcanzar el 100% de la población que disponga de teléfonos móviles.<br>+ OB_04 - Rastrear y gestionar la información de los usuarios de forma anónima. <br>+ OB_06 - Reducir el impacto de futuras pandemias en la sociedad. <br>+ OB_11 - Verificar de forma automática que los usuarios cumplen las cuarentenas impuestas. <br>+ OB_12 - Rastrear a los contactos estrechos de los usuarios. <br><br> Los procesos de negocio a implantar de los que depende son: <br> + PRI_02 - Establecer cuarentena y seguimiento. <br>+ PRI_03 - Rastrear contactos. <br>+ PRI_04 - Comprobar medidas sanitarias.|
|**Descripción**| Este subsistema agrupa los requisitos relacionados con la localización de las personas, ya sea por localización GPS o por triangulación por las antenas móviles. |
|**Importancia**| Alta. |
|**Prioridad**| Alta. |
|**Comentarios**| Este subsistema es fundamental para lograr reducir el impacto de una futura pandemia ya que será el encargado de rastrear la enfermedad a lo largo del país, y se podrán tomar medidas más específicas para las zonas que estén más afectadas. |

|**SUB_02**| **Gestor de notificaciones** |
| :---: | :--- |
|**Dependencias**| Los objetivos de negocio de los que depende son: <br>+ OB_02 - Alcanzar el 100% de la población que disponga de teléfonos móviles.<br>+ OB_03 - Alcanzar el mayor número de población posible. <br> + OB_07 -	Automatizar el proceso de citaciones para realizar pruebas médicas. <br>+ OB_08	- Informar a los usuarios que deben acudir a realizarse pruebas médicas. <br>+ OB_09 - Avisar a las fuerzas del orden si un usuario no acude a realizarse las pruebas médicas. <br>+ OB_10 - Avisar a las fuerzas del orden si un usuario no cumple con la cuarentena que se le ha impuesto. <br>+ OB_11 - Verificar de forma automática que los usuarios cumplen las cuarentenas impuestas.<br><br> Los procesos de negocio a implantar de los que depende son: <br>+ PRI_01 -  Realizar pruebas médicas. <br>+ PRI_02 - Establecer cuarentena y seguimiento. |
|**Descripción**| Este subsistema agrupa los requisitos relacionados con la notificación de avisos (cuarentena o cita médica) así como la gestión de formularios para avisar de casos positivos/sospechosos de personas cercanas que no dispongan de teléfono móvil. |
|**Importancia**| Alta. | 
|**Prioridad**| Alta. |
|**Comentarios**| Este subsistema es fundamental para lograr automatizar la mayoría de los procesos que existen en la actualidad y así lograr una mejor gestión de una futura pandemia. |

|**SUB_03**| **Gestor de estadísticas** |
| :---: | :--- |
|**Dependencias**| Los objetivos de negocio de los que depende son: <br> + OB_04 - Rastrear y gestionar la información de los usuarios de forma anónima. <br> + OB_05 - Preservar la privacidad de los usuarios. <br> + OB_13 - Mostrar un mapa de calor con las zonas de movilidad de los casos positivos. <br><br> Los procesos de negocio a implantar de los que depende son: <br>+ PRI_03 - Rastrear contactos. <br>+ PRI_04 - Comprobar medidas sanitarias.|
|**Descripción**| Este subsistema agrupa los requisitos relacionados con la gestión de los datos de ubicación de los casos diagnosticados como positivos y la actualización del mapa de calor que es básico para un mejor rastreo de una futura pandemia. |
|**Importancia**| Media |
|**Prioridad**| Media |
|**Comentarios**| Este subsistema es importante para poder obtener de forma detallada y exacta las zonas con un gran índice de casos y así poder tomar las medidas oportunas con el fin de evitar una propagación de la enfermedad hacia otras zonas. |

|**SUB_04**| **Gestor general** |
| :---: | :--- |
|**Dependencias**| Los objetivos de negocio de los que depende son: <br> + OB_02 - Alcanzar el 100% de la población que disponga de teléfonos móviles.<br>+ OB_03 - Alcanzar el mayor número de población posible. <br> + OB_14 - Coordinación entre CCAA y países.<br><br> Los procesos de negocio a implantar de los que depende son: <br>+ PRI_01 -  Realizar pruebas médicas. <br>+ PRI_02 - Establecer cuarentena y seguimiento. <br>+ PRI_03 - Rastrear contactos.|
|**Descripción**| Este subsistema agrupa los requisitos relacionados con la comunicación de los casos positivos entre CCAA (recordemos que la Sanidad está transferida a las CCAA y cada una de ellas tendrá su propia base de datos a las que no pueden acceder las demás) y a otros países; así como los cambios de dialecto y/o idioma (catalán, gallego, euskera, valenciano e inglés) dentro de la aplicación de Pandemio. |
|**Importancia**| Media. |
|**Prioridad**| Baja. |
|**Comentarios**| El número de personas que se desplacen entre comunidades o a otros países durante una futura pandemia será muy limitado como ha ocurrido en la actualidad. Además, aunque el español ahora no se considera lengua vehicular, la opción de poder cambiar de dialecto/idioma no se considera una prioridad. <br> Por estas dos razones se considera que este subsistema es de prioridad baja, pero de importancia media. |

<br>
<br>

# 6 CATÁLOGO DE REQUISITOS DEL SISTEMA A DESARROLLAR

## 6.1 Requisitos Generales del Sistema
Esta sección debería contener la especificación de los requisitos generales del sistema, también denominados características del sistema (system features) u objetivos del sistema. Sin embargo, ya que en clase no hemos diferenciado los objetivos del sistema de los objetivos de negocio, no entraremos en más detalle en esta sección y para cualquier referencia a los objetivos deberemos acudir al apartado "4.1 Objetivos de Negocio" donde ya se especificaron todos los objetivos y subobjetivos de Pandemio.


<br>

## 6.2 Casos de uso del Sistema 
Los casos de uso describen cómo utilizarán el sistema a desarrollar los futuros usuarios de Pandemio para realizar sus procesos de negocio. Esta sección se divide en las secciones que se describen a continuación:

### 6.2.1 Diagramas de Casos de Uso del Sistema
Los principales casos de uso que realizarán los futuros usuarios de Pandemio son los siguientes:

> Casos de uso de los sanitarios y rastreadores:
<p align="center">
  <img src="./Imágenes/Casos_de_uso_sanitarios.jpg">
</p>

> Casos de uso de las fuerzas del orden:
<p align="center">
  <img src="./Imágenes/Casos_de_uso_fuerzas_del_orden.jpg">
</p>

> Casos de uso del Gobierno de España:
<p align="center">
  <img src="./Imágenes/Casos_de_uso_gobierno.jpg">
</p>

> Casos de uso de los usuarios no identificados:
<p align="center">
  <img src="./Imágenes/Casos_de_uso_usuario_anonimo.jpg">
</p>



### 6.2.2 Especificación de Actores del Sistema
Todas las especificaciones de los actores que se han identificado en los casos de uso las encontramos en el apartado "4.2.1 Descripción de los Actores de Negocio a Implantar", por lo que no entraremos en más detalle en esta sección. 

### 6.2.3 Especificación de Casos de Uso del Sistema
A continuación, se especifican todos los casos de uso que se han identificado en el apartado "6.2.1 Diagramas de Casos de Uso del Sistema":

| CU_01 | Comprobar cuarentena |
| :--: | :----- |
|**Precondición**| Una persona debe permanecer en cuarentena y se le asigna a un sanitario su seguimiento. Además, el sanitario/rastreador debe estar logueado en la aplicación. |
|**Descripción**| Un sanitario/rastreador puede ver las personas que deben realizar cuarentena y comprobar que la están realizando. |
|**Secuencia Normal**| 1. El sanitario abre la aplicación. <br> 2. El sanitario elige la opción “Comprobar cuarentena”. <br> 3. La aplicación muestra una lista de personas en cuarentena. <br> 4. El sanitario busca en la lista a una persona. <br> 5. El sanitario entra a ver los detalles de esa persona. <br> 6. El sanitario solicita a esa persona que verifique su ubicación actual (CU_11). <br> 7. El sistema muestra la ubicación que ha enviado la persona. <br> 8. El sanitario comprueba la ubicación para verificar que la persona está cumpliendo la cuarentena. |
|**Postcondición**| La persona ha verificado su ubicación actual y queda reflejado en el sistema. |
|**Excepciones**| 3a. Si el sanitario no tiene ningún paciente en cuarentena se muestra una lista vacía. <br> 6a. La persona no verifica su ubicación actual. <br> &nbsp;&nbsp;&nbsp; 6a.1. El sanitario escoge la opción "Avisar incumplimiento cuarentena". <br> &nbsp;&nbsp;&nbsp; 6a.2.El sanitario añade comentarios si es necesario. <br> &nbsp;&nbsp;&nbsp; 6a.3. El sanitario envía el aviso a las fuerzas del orden. <br> 6b. La persona no dispone de teléfono móvil. <br> &nbsp;&nbsp;&nbsp; 6b.1. El sanitario escoge la opción "Avisar incumplimiento cuarentena". <br> &nbsp;&nbsp;&nbsp; 6b.2.El sanitario añade un comentario explicando que la persona no dispone de teléfono móvil. <br> &nbsp;&nbsp;&nbsp; 6b.3. El sanitario envía el aviso a las fuerzas del orden. <br> 8a. La persona verifica su ubicación actual pero no está cumpliendo la cuarentena impuesta. <br> &nbsp;&nbsp;&nbsp; 8a.1. El sanitario escoge la opción "Avisar incumplimiento cuarentena". <br> &nbsp;&nbsp;&nbsp; 8a.2.El sanitario añade comentarios si es necesario. <br> &nbsp;&nbsp;&nbsp; 6b.3. El sanitario envía el aviso a las fuerzas del orden. |
|**Importancia**| Alta. |
|**Prioridad**| Alta. |

| CU_02 | Ver avisos fuerzas del orden |
| :--: | :----- |
|**Precondición**| El sanitario ha avisado previamente a las fuerzas del orden para informarles de un caso que no está cumpliendo la cuarentena o no ha asistido a una cita médica. Además, el sanitario debe estar logueado en la aplicación. |
|**Descripción**| Un sanitario/rastreador puede ver los avisos que han emitido las fuerzas del orden sobre un caso que ha abierto ese sanitario previamente. |
|**Secuencia Normal**| 1. El sanitario abre la aplicación. <br> 2. El sanitario elige la opción “Ver avisos fuerzas del orden”. <br> 3. La aplicación muestra todos los avisos que hayan emitido las fuerzas del orden sobre casos abiertos previamente por el sanitario. <br> 4. El sanitario abre un aviso para ver los detalles y las nuevas noticias sobre el caso. |
|**Postcondición**| El sanitario visualiza los detalles de uno de los casos que tiene abiertos. |
|**Excepciones**| 3a. Si el sanitario no tiene ningún caso abierto se muestra una lista vacía.  |
|**Importancia**| Media. |
|**Prioridad**| Media. |

| CU_03 | Ver citas médicas |
| :--: | :----- |
|**Precondición**| El sanitario debe estar previamente logueado y tiene citas médicas fijadas con pacientes.  |
|**Descripción**| Un sanitario/rastreador puede ver la fecha, hora e historial médico del paciente de las citas que tiene programadas. |
|**Secuencia Normal**| 1. El sanitario abre la aplicación. <br> 2. El sanitario elige la opción “Ver citas médicas”. <br> 3. La aplicación muestra fecha, hora y nombre de los pacientes con citas programadas.  <br> 4. Un paciente acude a su cita médica.  <br> 5. El sanitario entra a ver los detalles de ese paciente. <br> 6. El sanitario actualiza el historial médico del paciente. |
|**Postcondición**| El sanitario visualiza la agenda de citas programadas y actualiza cada una de ellas. |
|**Excepciones**| 3a. Si el sanitario no tiene ninguna cita programada se muestra una lista vacía.  <br> 4a. El paciente no acude a la cita médica que tiene programada. <br> &nbsp;&nbsp;&nbsp; 4a.1. El sanitario escoge la opción "Avisar incumplimiento cita médica". <br> &nbsp;&nbsp;&nbsp; 4a.2.El sanitario añade comentarios si es necesario. <br> &nbsp;&nbsp;&nbsp; 4a.3. El sanitario envía el aviso a las fuerzas del orden. |
|**Importancia**| Alta. |
|**Prioridad**| Alta. |

| CU_04 | Ver avisos |
| :--: | :----- |
|**Precondición**| El usuario de las fuerzas del orden debe estar logueado. |
|**Descripción**| El usuario de las fuerzas del orden accede a una lista con los avisos de los sanitarios sobre personas que o bien no cumplen cuarentena o bien no han acudido a su cita médica. |
|**Secuencia Normal**| 1. El usuario de las fuerzas del orden abre la aplicación. <br> 2. Elige la opción “Ver avisos”. <br> 3. La aplicación muestra todos los avisos que hayan emitido los sanitarios. <br> 4. El usuario de las fuerzas del orden abre un caso <br> 5.El usuario de las fuerzas del orden investiga el caso. <br> 6. El usuario de las fuerzas del orden actualiza el caso. <br> 7. El usuario de las fuerzas del orden cierra el caso. |
|**Postcondición**| El usuario de las fuerzas del orden visualiza los avisos realizados por los sanitarios y los actualiza. |
|**Excepciones**| 3a. Si no hubiera ningún aviso sanitario se muestra una lista vacía.  |
|**Importancia**| Alta. |
|**Prioridad**| Alta. |

| CU_05 | Revisar incidencia |
| :--: | :----- |
|**Precondición**| Es necesario estar logueado en la aplicación. |
|**Descripción**| El Gobierno de España puede ver estadísticas generales y por zonas, además de un mapa de calor, para ver qué zonas están más afectadas y tomar las medidas necesarias en función de esos datos. |
|**Secuencia Normal**| 1. El Gobierno abre la aplicación. <br> 2. Elige la opción “Revisar incidencia”. <br> 3. La aplicación muestra estadísticas generales y de las zonas más afectadas.  |
|**Postcondición**| En función de los datos obtenidos, se toman las medidas necesarias para reducir el impacto de la nueva pandemia en la población. |
|**Excepciones**| Ninguna. |
|**Importancia**| Alta. |
|**Prioridad**| Media. |

| CU_06 | Ver citas médicas propias |
| :--: | :----- |
|**Precondición**| Un usuario está pendiente de acudir a una cita médica. |
|**Descripción**| Un usuario de la aplicación de Pandemio puede ver la fecha, hora y lugar de la cita médica que tiene asignada. |
|**Secuencia Normal**| 1. El usuario abre la aplicación. <br> 2. El usuario elige la opción “Ver citas médicas propias”. <br> 3. La aplicación muestra la fecha, hora y lugar donde debe acudir a la cita médica. |
|**Postcondición**| El usuario ve la fecha, hora y lugar de la cita médica que tiene asignada. |
|**Excepciones**| 3a. Si el usuario no tiene que cumplir ninguna cita médica asignada se muestra un mensaje avisándole.  <br> 3b. Si el usuario ha informado de un caso cercano positivo sin móvil, el sistema especificará en el aviso quién debe acudir a la cita médica. |
|**Importancia**| Alta. |
|**Prioridad**| Alta. |


| CU_07 | Ver cuarentena establecida |
| :--: | :----- |
|**Precondición**| Un usuario está pendiente de realizarse pruebas médicas o se le ha establecido una cuarentena sanitaria. |
|**Descripción**| Un usuario de la aplicación de Pandemio puede ver cuantos días de cuarentena tiene que realizar. |
|**Secuencia Normal**| 1. El usuario abre la aplicación. <br> 2. El usuario elige la opción “Ver cuarentena establecida”. <br> 3. La aplicación muestra el número de días que quedan de cuarentena y la fecha en la que termina. |
|**Postcondición**| El usuario ve el número de días que le quedan para cumplir la cuarentena. |
|**Excepciones**| 3a. Si el usuario no tiene que cumplir ninguna cuarentena se muestra un mensaje avisándole.  <br> 3b. Si el usuario ha informado de un caso cercano positivo sin móvil, el sistema especificará en el aviso quién debe cumplir la cuarentena establecida y hasta qué fecha. |
|**Importancia**| Alta. |
|**Prioridad**| Alta. |


| CU_08 | Informar de caso cercano positivo sin móvil |
| :--: | :----- |
|**Precondición**| Un usuario tiene a su cargo a una persona que no dispone de teléfono móvil. |
|**Descripción**| Un usuario de la aplicación de Pandemio puede informar de un caso positivo para una persona dependiente que no dispone de teléfono móvil. |
|**Secuencia Normal**| 1. El usuario abre la aplicación. <br> 2. El usuario elige la opción “Informar de caso cercano positivo sin móvil”. <br> 3. El usuario rellena los datos que pide la aplicación. <br> 4. El usuario envía el formulario. <br> 5. La aplicación comprueba que los datos introducidos son correctos. <br> 6. La aplicación procesa el formulario y genera una cita médica. <br> 7. La aplicación muestra un mensaje con la cita médica creada. |
|**Postcondición**| Se ha creado una cita médica que se puede ver en ese momento o después en la opción “Ver citas médicas propias” (CU_06). |
|**Excepciones**| 5a. El formulario está mal rellenado o contiene algún error. <br> &nbsp;&nbsp;&nbsp; 5a.1. La aplicación muestra un mensaje de error con el motivo del fallo. <br> &nbsp;&nbsp;&nbsp; 5a.2. Volver al paso 3. |
|**Importancia**| Media. |
|**Prioridad**| Baja. |


| CU_09 | Informar de síntomas compatibles |
| :--: | :----- |
|**Precondición**| Un usuario comienza a tener síntomas compatibles con la nueva pandemia. |
|**Descripción**| Un usuario de la aplicación de Pandemio puede informar de que comienza a desarrollar síntomas compatibles con la nueva enfermedad. |
|**Secuencia Normal**| 1. El usuario abre la aplicación. <br> 2. El usuario elige la opción “Informar de síntomas compatibles”. <br> 3. El usuario rellena los datos que pide la aplicación. <br> 4. El usuario envía el formulario. <br> 5. La aplicación comprueba que los datos introducidos son correctos. <br> 6. La aplicación procesa el formulario y genera una cita médica. <br> 7. La aplicación muestra un mensaje con la cita médica creada. |
|**Postcondición**| Se ha creado una cita médica que se puede ver en ese momento o después en la opción “Ver citas médicas propias” (CU_06). |
|**Excepciones**| 5a. El formulario está mal rellenado o contiene algún error. <br> &nbsp;&nbsp;&nbsp; 5a.1. La aplicación muestra un mensaje de error con el motivo del fallo. <br>&nbsp;&nbsp;&nbsp; 5a.2. Volver al paso 3. |
|**Importancia**| Media. |
|**Prioridad**| Baja. |


| CU_10 | Ver mapa calor |
| :--: | :----- |
|**Precondición**| Ninguna. |
|**Descripción**| Un usuario de la aplicación de Pandemio puede ver un mapa de calor para ver las zonas donde ha habido un gran número de casos positivos y así evitar esas zonas. |
|**Secuencia Normal**| 1. El usuario abre la aplicación. <br> 2. El usuario elige la opción “Ver mapa de calor”. <br> 3. El sistema muestra un mapa de calor de la zona donde se encuentra el usuario acompañado con una leyenda de colores para ver el impacto de la nueva pandemia en la zona. |
|**Postcondición**| El usuario ve el mapa de calor de la zona donde se encuentra.  |
|**Excepciones**| Ninguna. |
|**Importancia**| Media. |
|**Prioridad**| Media. |


| CU_11 | Enviar ubicación |
| :--: | :----- |
|**Precondición**| Un sanitario o rastreador solicita a un usuario que mande la ubicación donde se encuentra. |
|**Descripción**| Un usuario de la aplicación de Pandemio debe mandar la ubicación donde se encuentra para confirmar que está cumpliendo la cuarentena si un sanitario o rastreador se lo pide. |
|**Secuencia Normal**| 1. El usuario abre la aplicación. <br> 2. El usuario elige la opción “Enviar ubicación”. <br> 3. El usuario coloca su huella en el sensor de huellas del teléfono móvil. <br> 4. La aplicación valida la huella colocada. <br> 5. La aplicación envía la ubicación del teléfono móvil al sanitario o rastreador correspondiente para que verifique si es correcta o no.  |
|**Postcondición**| Ubicación enviada correctamente.  |
|**Excepciones**| 3a. El usuario utiliza el reconocimiento facial de su teléfono móvil. <br> &nbsp;&nbsp;&nbsp; 3a.1. La aplicación valida la cara reconocida. <br> &nbsp;&nbsp;&nbsp; 3a.2. La aplicación envía la ubicación del teléfono móvil al sanitario o rastreador correspondiente. <br> 4a. La huella o la cara introducidas no se corresponden con el usuario que ha solicitado el sanitario. <br> &nbsp;&nbsp;&nbsp; 4a.1. La aplicación muestra un mensaje de error con el motivo del fallo. <br> &nbsp;&nbsp;&nbsp; 4a.2. Volver al paso 3. |
|**Importancia**| Alta. |
|**Prioridad**| Alta. |


<br>

## 6.3 Requisitos Funcionales del Sistema
Esta sección contiene todos los requisitos funcionales del sistema que se han identificado a partir de los objetivos de negocio.

### 6.3.1 Requisitos de Información del Sistema
Estos requisitos especifican qué información debe almacenar el sistema para poder ofrecer la funcionalidad descrita en los casos de uso del sistema o en otros requisitos:

| **ID** | **Nombre** | **Descripción** |
| :--: | :----- |:----- |
|**RFI_01**| Historial de ubicación | El sistema almacenará el historial de ubicación de cada teléfono móvil el número de días que establezcan los criterios estrictamente epidemiológicos. |
|**RFI_02**| Historial médico | El sistema almacenará el historial médico de todos los ciudadanos que viven en España. |
|**RFI_03**| Listado personas en cuarentena | El sistema almacenará un listado de todas las personas que estén en cuarentena. |
|**RFI_04**| Listado personas pendientes de cita médica | El sistema almacenará un listado de todas las personas que tengan una cita médica pendiente. |
|**RFI_05**| Historial usuario | El sistema almacenará un historial de los datos a los que ha accedido cada usuario registrado en el sistema. |
|**RFI_06**| Historial de seguridad | El sistema almacenará un registro cuando ocurra alguno de los siguientes eventos: entrada al sistema por parte de un usuario, 2 o más intentos fallidos al introducir la contraseña de usuario, y cambio de contraseña de usuario. | 
 
 
### 6.3.2 Requisitos de Reglas de Negocio del Sistema
Estos requisitos especifican qué reglas de negocio, políticas y restricciones debe respetar el sistema, evitando que se incumplan durante su funcionamiento:

| **ID** | **Nombre** | **Descripción** |
| :--: | :----- |:----- |
|**RFN_01**| Protección de datos | El nuevo sistema debe cumplir con las leyes y reglamentos establecidos por cada comunidad autónoma para la protección de datos. |
|**RFN_02**| Leyes generales | El nuevo sistema se acogerá a las leyes generales públicas. |
|**RFN_03**| Acceso restringido a datos sensibles | Solo los usuarios logueados podrán acceder a los datos sensibles que almacena el sistema. Para ello, las personas encargadas de la gestión de la pandemia en el Gobierno de España, todos los sanitarios y rastreadores, y todos el personal de las fuerzas del orden deberán registrarse en la aplicación. |
|**RFN_04**| Validación de nuevos registros | La validación de los nuevos registros solo la realizarán los superadministradores del Gobierno de España. |
|**RFN_05**| Almacenamiento triplicado de los datos | Cada CCAA tendrá 3 copias de todos los datos y usará 3 servidores de datos diferentes para almacenar cada copia de los datos. |
|**RFN_06**| Gestión propia de bases de datos | Cada comunidad autónoma gestionará sus propias bases de datos. |
|**RFN_07**| Revelación datos sensibles | El sistema solo revelará los datos sensibles imprescindibles a los usuarios logueados. |
|**RFN_08**| Acceso al historial médico | Los sanitarios podrán acceder al historial médico de los pacientes. |
|**RFN_09**| Aviso incumplimiento cita médica | Los sanitarios y rastreadores deberán avisar a las fuerzas del orden si una persona no acude a una cita médica. |
|**RFN_10**| Aviso incumplimiento cuarentena | Los sanitarios y rastreadores deberán avisar a las fuerzas del orden si una persona no cumple la cuarentena asignada. |
|**RFN_11**| Comprobación cuarentena | Los sanitarios y rastreadores deberán comprobar que los casos diagnosticados como positivos cumplen la cuarentena establecida. |
|**RFN_12**| Campañas publicitarias | El Ministerio de Sanidad deberá crear campañas publicitarias para fomentar que las personas con dispositivos móviles informen de casos positivos (de las personas dependientes que tengan a su cargo que no dispongan de teléfono móvil) o si comienzan a desarrollar algún síntoma. |
|**RN_13**| Geolocalización | El sistema utilizará localización por triangulación de antenas móviles si puede garantizar una "cercanía" de distancia menor a 5 metros, si no utlilizará la localización por GPS. |
|**RFN_14**| Geolocalización en modo avión | El sistema solo almacenará la ubicación obtenida por GPS si el teléfono móvil está en modo avión. |
|**RFN_15**| Instalación automática | La aplicación se instalará automaticamente en todos los teléfono móviles independientemente del sistema operativo que utilicen. |


### 6.3.3 Requisitos de Conducta del Sistema
Estos requisitos especifican cualquier otro comportamiento deseado del sistema que no se haya especificado mediante los casos de uso del sistema, como generación de informes, funcionalidades transversales a varios casos de uso del sistema, etc. También describen los servicios que debe ofrecer el sistema para que los usuarios u otros sistemas puedan realizar sus tareas de negocio:

| **ID** | **Nombre** | **Descripción** |
| :--: | :----- |:----- |
|**RFC_01**| Automatización de citas médicas | El sistema generará citas médicas automáticas para el centro de salud más cercano cuando una persona haya estado en contacto con un positivo, o se informe de un positivo de un caso cercano sin teléfono móvil, o se informe de síntomas compatibles. |
|**RFC_02**| Notificación cita médica caso cercano | El sistema enviará una notificación PUSH al usuario para que acuda a realizarse pruebas médicas si ha estado en contacto con un caso positivo. |
|**RFC_03**| Notificación cita médica mediante formulario | El sistema enviará una notificación PUSH al usuario para que acuda a realizarse pruebas médicas si informa de un positivo de un caso cercano sin teléfono móvil o si informa de síntomas compatibles. |
|**RFC_04**| Notificación días de cuarentena | El sistema enviará una notificación PUSH a los usuarios que deban realizar la cuarentena informándoles del número de días de cuarentena que deben cumplir. |
|**RFC_05**| Mapa de calor | El sistema generará un mapa de calor con los datos de usuarios que hayan sido diagnosticados como positivos. |
|**RFC_06**| Actualización del mapa de calor | El mapa de calor se actualizará cada hora. |
|**RFC_07**| Valor mínimo mapa de calor | El número mínimo de personas contagiadas que deben pasar por una zona para que esta aparezca coloreada en el mapa de calor será de 5 personas. |
|**RFC_08**| Colores leyenda mapa de calor | El mapa de calor se coloreará con colores que vayan desde el amarillo hasta el rojo en función del número de casos positivos que haya en la zona. |
|**RFC_09**| Validación automática de formularios | El sistema validará automáticamente los formularios emitidos por el usuario cuando avise de casos positivos cercanos y no dejará enviarlos en caso de que exista algún error. |
|**RFC_10**| Notificación entre CCAA | El sistema notificará a las CCAA si un caso positivo se ha movido entre comunidades. |
|**RFC_11**| Informe casos positivos desplazados | El sistema generará un informe con los casos positivos que hayan salido del país para comunicárselo lo antes posible. |
|**RFC_12**| Informe datos mapa de calor | El sistema generará un informe con los datos detallados obtenidos en el mapa de calor y solo podrá acceder a él el Gobierno. |
|**RFC_13**| Notificación incumplimiento de la cuarentena | El sistema enviará una notificación PUSH a las fuerzas del orden si un sanitario avisa de que un usuario está incumplimiento la cuarentena. |
|**RFC_14**| Notificación incumplimiento de la cita médica | El sistema enviará una notificación PUSH a las fuerzas del orden si un sanitario avisa de que un usuario no ha acudido a una cita médica. |

<br>

## 6.4 Requisitos No Funcionales del Sistema
Esta sección contiene todos los requisitos no funcionales del sistema que se han identificado a partir de los objetivos de negocio.

### 6.4.1 Requisitos de Fiabilidad
Estos requisitos establecen, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como recuperabilidad y tolerancia a fallos: 

| **ID** | **Nombre** | **Descripción** |
| :--: | :----- |:----- |
|**RNFF_01**| Alta disponibilidad | Disponibilidad de al menos el 99,99% de las veces. |
|**RNFF_02**| Tiempo de inicio | El tiempo de inicio o reinicio del sistema debe ser inferior a dos minutos. |
|**RNFF_03**| Baja probabilidad de fallo | La probabilidad de fallo será inferior al 3%. |
|**RNFF_04**| Copia de los datos | Cada CCAA tendrá 3 copias de todos los datos y usará 3 servidores de datos diferentes para almacenar cada copia de los datos. |
|**RNFF_05**| Sincronización de datos | Se sincronizarán los datos de todos los servidores cada 5 minutos. |


### 6.4.2 Requisitos de Usabilidad
Estos requisitos establecen, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como facilidad de aprendizaje, comprensión, operatividad y atractividad:

| **ID** | **Nombre** | **Descripción** |
| :--: | :----- |:----- |
|**RNFU_01**| Bajo tiempo de aprendizaje | El tiempo de aprendizaje del sistema debe ser inferior a 2 horas. |
|**RNFU_02**| Manuales de usuario | El sistema debe contar con manuales de usuario y ayuda online. |
|**RNFU_03**| Clarificación de errores | El sistema proporcionará errores claros y concisos. |
|**RNFU_04**| Múltiples idiomas | Los usuarios podrán cambiar el dialecto o el idioma de la aplicación pudiendo elegir entre español, catalán, valenciano, gallego, euskera e inglés. |
|**RNFU_05**| Fácil acceso a la información deseada | El sistema deberá permitir en el 80% de las veces que, con un máximo de 5 clicks, se pueda llegar a la información deseada. |

### 6.4.3 Requisitos de Eficiencia
Estos requisitos establecen, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como tiempo de respuesta:

| **ID** | **Nombre** | **Descripción** |
| :--: | :----- |:----- |
|**RNFE_01**| Transacciones múltiples | El sistema debe ser capaz de procesar 15 millones de transacciones por minuto. |
|**RNFE_02**| Rápida respuesta | Toda transacción debe responder al usuario en menos de 10 segundos. |
|**RNFE_03**| Conexiones simultáneas | El sistema debe soportar 5 millones de conexiones simultáneas. |
|**RNFE_04**| Máximo tiempo de respuesta | El sistema deberá tener un tiempo máximo de respuesta de 5 segundos para cualquier operación de consulta. |

### 6.4.4 Requisitos de Mantenibilidad
Estos requisitos establecen, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como estabilidad, facilidad de análisis, facilidad de cambio, facilidad de pruebas:

| **ID** | **Nombre** | **Descripción** |
| :--: | :----- |:----- |
|**RNFM_01**| Código fuente público | El código de la aplicación será publicado en GitHub y sin patentes para que cualquier usuario pueda buscar fallos en la aplicación y ayudar a su mejora. |
|**RNFM_02**| Actualizaciones forzadas | Se forzará la actualización de la aplicación si se identifica algún bug que pueda afectar al sistema. |
|**RNFM_03**| Lenguaje Java | El código fuente que se implemente en JAVA deberá cumplir las recomendaciones de Code Conventions for the Java Programming Language. |

### 6.4.5 Requisitos de Portabilidad
Estos requisitos establecen, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos relacionados con la escalabilidad (capacidad de instalación, capacidad de sustitución, adaptabilidad, coexistencia, compatibilidad con hardware o software, etc):

| **ID** | **Nombre** | **Descripción** |
| :--: | :----- |:----- |
|**RNFP_01**| Instalación automática | La aplicación se instalará automaticamente en todos los teléfono móviles independientemente del sistema operativo que utilicen.|
|**RNFP_02**| Implantación en centros de salud | La aplicación se instalará en todos los ordenadores de los centros de salud y coexistirá con las aplicaciones sanitarias propias de cada CCAA.|
|**RNFP_03**| Compatibilidad entre sistemas | El uso de está aplicación es compatible con el uso de cualquier otra aplicación.|
|**RNFP_04**| Extensiones de SQL | El sistema deberá evitar el uso de extensiones propietarias al estándar SQL-92 en el sistema de gestión de bases de datos que utilice.|

### 6.4.6 Requisitos de Seguridad
Estos requisitos establecen, de la manera más objetiva y medible posible, los niveles que debe cumplir el sistema a desarrollar en aspectos como accesos al sistema, identificación y autenticación, protección de datos y privacidad:

| **ID** | **Nombre** | **Descripción** |
| :--: | :----- |:----- |
|**RNFS_01**| Modificación de permisos | Los permisos de acceso solo pueden ser modificados por los administradores.|
|**RNFS_02**| Validación de nuevos registros | La validación de los nuevos registros solo la realizarán los superadministradores del Gobierno de España.|
|**RNFS_03**| Patrones de seguridad | El sistema debe seguir patrones de seguridad que incrementen la seguridad.|
|**RNFS_04**| Protección frente a accesos no autorizados | El sistema debe asegurar que los datos están protegidos de accesos no autorizados.|
|**RNFS_05**| Control de acceso | El sistema controlará el acceso y lo permitirá solamente a usuarios autorizados.|
|**RNFS_06**| Credenciales de acceso | Los usuarios accederán al sistema con un nombre de usuario y contraseña.|
|**RNFS_07**| Registro en lista de seguridad | El sistema guardará un registro en una lista cada vez que ocurra alguno de los siguientes eventos: entrada al sistema por parte de un usuario, 2 o más intentos fallidos al introducir la contraseña de usuario, y cambio de contraseña de usuario.|
|**RNFS_08**| Ataques por inyección de SQL | El sistema deberá ser capaz de evitar ataques de inyección de SQL sistemáticos.|
|**RNFS_09**| Codificación de contraseñas | Las contraseñas serán almacenadas en las bases de datos usando un algoritmo criptográfico para que no sean visibles a simple vista.|

### 6.4.7 Otros Requisitos No Funcionales
Esta sección contiene otros requisitos no funcionales que se han identificado y que no pertenecen a ninguna de las categorías anteriores: 

| **ID** | **Nombre** | **Descripción** |
| :--: | :----- |:----- |
|**RNFO_01**| Aplicación en segundo plano | No será necesario tener la aplicación abierta en los dispositivos móviles para que funcione correctamente.|
|**RNFO_02**| Tipos de formularios | La aplicación debe contar con dos formularios, uno para informar de un caso positivo cercano de una persona dependiente, y otro para informar de síntomas compatibles. Estos formularios no se podrán enviar si contienen algún error y será el propio sistema el encargado de validarlos y gestionarlos.|

<br>
  
## 6.5 Restricciones Técnicas del Sistema
Esta sección contiene las restricciones técnicas que se imponen al sistema software a desarrollar (tecnología a usar, protocolos de comunicaciones, compatibilidad con navegadores, etc.):

  | **ID** | **Nombre** | **Descripción** |
  | :--: | :----- |:----- |
  |**RT_01**| Motor de la base de datos | El motor de la base de datos donde se almacenará toda la información será MySQL. |
  |**RT_02**| Código de la aplicación | El código de la aplicación estará escrito en Kotlin y XML para la parte de cliente, y Java para la parte de servidor. |
  |**RT_03**| Formas geolocalización | El sistema utilizará la ubicación por GPS y/o por triangulación de antenas móviles. |
  |**RT_04**| Intercambio de datos vía Internet | Cualquier intercambio de datos vía Internet que realice el software se realizará por medio del protocolo encriptado HTTPS. |
  |**RT_05**| Servidores | Los servidores usados para almacenar datos serán MySQL server, PostgreSQL server y MongoDB server. |
  |**RT_06**| Compatibilidad de SO | La aplicación será compatible en todos los SO de los teléfonos móviles (Android, iOS, HarmonyOS, etc.) y en cualquier navegador (Windows, Linux, etc.). |
  
<br>  
  
## 6.6 Requisitos de Integración del Sistema
Estos requisitos identifican aquellos servicios disponibles en el entorno tecnológico de producción o componentes software cuya funcionalidad es relevante para el sistema a desarrollar y deben ser consumidos por el mismo:
  
   | **ID** | **Nombre** | **Descripción** |
   | :--: | :----- |:----- |
   |**RI_01**| Servicio @firma | El sistema deberá utilizar el servicio @firma para todos los aspectos relacionados con validación y firma electrónica. |
   |**RI_02**| Servicio 'Dni electrónico' | El sistema deberá utilizar el servicio 'Dni electrónico' para todos los aspectos relacionados con la validación del DNI. |
   
<br>

## 6.7 Información Sobre Trazabilidad
Finalmente, se muestran todas las matrices de trazabilidad que hemos considerado oportunas para identificar las relaciones entre los requisitos identificados:

>	Matriz de trazabilidad de Casos de Uso frente a Objetivos de Negocio.

 | **ID** | **Nombre** | **Nivel de complejidad** | **Nivel de prioridad** | **Objetivos de Negocio** |
 | :--: | :----- | :-----: | :-----: | :----- |
 | **CU_01** | Comprobar cuarentena | Alto | Alto | OB_10,OB_11 |
 | **CU_02** | Ver avisos fuerzas del orden| Medio | Medio | OB_09,OB_10 |
 | **CU_03** | Ver citas médicas | Medio | Alto | OB_09 |
 | **CU_04** | Ver avisos | Medio | Alto | OB_09,OB_10 |
 | **CU_05** | Revisar incidencia| Alto | Medio | OB_06,OB_13,OB_14 |
 | **CU_06** | Ver citas médicas propias | Bajo | Alto | OB_02,OB_03,OB_07,OB_08|
 | **CU_07** | Ver cuarentena establecida| Bajo | Alto | OB_02,OB_03|
 | **CU_08** | Informar de caso cercano positivo sin móvil | Bajo | Bajo | OB_02,OB_03,OB_04,OB_05,OB_07,OB_08 |
 | **CU_09** | Informar de síntomas compatibles | Bajo | Bajo | OB_02,OB_03,OB_04,OB_05,OB_07,OB_08|
 | **CU_10** | Ver mapa calor | Alto | Medio | OB_02,OB_04,OB_05,OB_06,OB_13 |
 | **CU_11** | Enviar ubicación | Medio | Alto  | OB_02,OB_03 |

<br>

>	Matriz de trazabilidad de Requisitos de Información frente a Objetivos de Negocio.

 | **ID** | **Nombre**  | **Nivel de complejidad** | **Nivel de prioridad** | **Objetivos de Negocio** |
 | :--: | :----- | :-----: | :-----: | :----- |
 | **RFI_01** | Historial de ubicación | Alto | Alto | OB_04 |  
 | **RFI_02** | Historial médico | Medio | Bajo | OB_04,OB_07 |  
 | **RFI_03** | Listado personas en cuarentena | Medio | Alto | OB_10,OB_11 |  
 | **RFI_04** | Listado personas pendientes de cita médica | Medio | Alto | OB_07,OB_08,OB_09 |  
 | **RFI_05** | Historial usuario | Medio | Bajo | OB_04,OB_05 | 
 |**RFI_06**| Historial de seguridad | Medio | Alto | OB_05 |
 
 
 <br>

>	Matriz de trazabilidad de Reglas de Negocio frente a Objetivos de Negocio.

| **ID** | **Nombre** | **Nivel de complejidad** | **Nivel de prioridad** | **Objetivos de Negocio** |
 | :--: | :-----  | :-----: | :-----: | :----- |
 | **RFN_01** | Protección de datos | Medio | Alto | OB_04 |
 | **RFN_02** | Leyes generales| Medio | Alto | OB_04 |  
 | **RFN_03** | Acceso restringido a datos sensibles | Alto | Alto | OB_04,OB_05 |     
 | **RFN_04** | Validación de nuevos registros | Alto | Alto | OB_05 |  
 | **RFN_05** | Almacenamiento triplicado de los datos | Alto | Medio | OB_04 |  
 | **RFN_06** | Gestión propia de bases de datos | Medio | Medio | OB_04,OB_14 |    
 | **RFN_07** | Revelación datos sensibles | Alto | Alto | OB_04 |  
 | **RFN_08** | Acceso al historial médico | Medio | Medio | OB_04,OB_05 |  
 | **RFN_09** | Aviso incumplimiento cita médica | Medio | Alto | OB_09 |     
 | **RFN_10** | Aviso incumplimiento cuarentena | Medio | Alto | OB_10 |
 | **RFN_11** | Comprobación cuarentena | Alto | Medio | OB_11|  
 | **RFN_12** | Campañas publicitarias | Bajo| Bajo | OB_03,OB_06|    
 | **RFN_13** | Geolocalización | Alto | Alto | OB_02,OB_04|  
 | **RFN_14** | Geolocalización en modo avión | Alto | Alto | OB_02,OB_04 | 
 | **RFN_15** | Instalación automática | Alto | Alto | OB_02 | 

<br>

>	Matriz de trazabilidad de Requisitos de Conducta frente a Objetivos de Negocio.

 | **ID** | **Nombre** | **Nivel de complejidad** | **Nivel de prioridad** | **Objetivos de Negocio** |
 | :--: |  :----- | :-----: | :-----: | :-----|
 | **RFC_01** | Automatización de citas médicas | Alto | Alto | OB_03,OB_07,OB_08,OB_12 |  
 | **RFC_02** | Notificación cita médica caso cercano | Bajo | Medio | OB_08,OB_12 |  
 | **RFC_03** | Notificación cita médica mediante formulario | Bajo | Medio | OB_07,OB_12 | 
 | **RFC_04** | Notificación días de cuarentena | Bajo | Medio | OB_08 |  
 | **RFC_05** | Mapa de calor | Alto | Bajo | OB_13 |  
 | **RFC_06** | Actualización del mapa de calor | Medio | Bajo | OB_13 |     
 | **RFC_07** | Valor mínimo mapa de calor | Alto | Bajo | OB_13 |   
 | **RFC_08** | Colores leyenda mapa de calor | Bajo | Bajo | OB_13 |  
 | **RFC_09** | Validación automática de formularios | Medio | Medio | OB_07 |     
 | **RFC_10** | Notificación entre CCAA | Alto | Alto | OB_14 |  
 | **RFC_11** |	Informe casos positivos desplazados  | Bajo | Alto | OB_14 |  
 | **RFC_12** | Informe datos mapa de calor | Alto | Alto | OB_14 |     
 | **RFC_13** | Notificación incumplimiento de la cuarentena | Bajo | Alto | OB_10 |  
 | **RFC_14** | Notificación incumplimiento de la cita médica | Bajo | Alto | OB_09 |   

<br>

>	Matriz de trazabilidad de Requisitos no Funcionales frente a Objetivos de Negocio.

 | **ID** | **Nombre** | **Nivel de complejidad** | **Nivel de prioridad** | **Objetivos de Negocio** |
 | :--: |  :----- | :-----: | :-----: | :----- |
 | **RNFF_01** | Alta disponibilidad | Alto | Alto | OB_01,OB_02,OB_06 |  
 | **RNFF_02** | Tiempo de inicio | Alto | Medio | OB_01,OB_06 |  
 | **RNFF_03** | Baja probabilidad de fallo | Alto | Alto | OB_01,OB_06 |    
 | **RNFF_04** | Copia de los datos | Alto | Medio | OB_01,OB_06,OB_14 |  
 | **RNFF_05** | Sincronización de datos | Alto | Alto | OB_01,OB_04,OB_06,OB_14 |  
 | **RNFU_01** | Bajo tiempo de aprendizaje | Bajo | Bajo | OB_01,OB_02 |     
 | **RNFU_02** | Manuales de usuario | Medio | Alto | OB_01,OB_02 |   
 | **RNFU_03** | Clarificación de errores| Alto | Alto | OB_01,OB_02 |  
 | **RNFU_04** | Múltiples idiomas| Bajo | Bajo | OB_01,OB_02 |     
 | **RNFU_05** | Fácil acceso a la información deseada | Medio | Bajo | OB_01,OB_02 |  
 | **RNFE_01** | Transacciones múltiples | Alto | Alto | OB_01 |  
 | **RNFE_02** | Rápida respuesta | Alto | Medio | OB_01 |     
 | **RNFE_03** | Conexiones simultáneas | Alto | Alto | OB_01 |  
 | **RNFE_04** | Máximo tiempo de respuesta | Alto | Medio | OB_01 |
 | **RNFM_01** | Código fuente público | Bajo | Bajo | OB_01,OB_06 |  
 | **RNFM_02** | Actualizaciones forzadas | Bajo | Medio | OB_01,OB_06 |  
 | **RNFM_03** | Lenguaje Java | Medio | Medio | OB_01 |      
 | **RNFP_01** | Instalación automática | Alto | Alto | OB_01,OB_02,OB_06 |  
 | **RNFP_02** | Implantación en centros de salud | Alto | Alto | OB_01,OB_06 |     
 | **RNFP_03** | Compatibilidad entre sistemas | Alto | Alto | OB_01,OB_06 |   
 | **RNFP_04** | Extensiones de SQL | Bajo | Bajo | OB_01,OB_02,OB_06 |  
 | **RNFS_01** | Modificación de permisos | Bajo | Alto | OB_01,OB_05 |     
 | **RNFS_02** | Validación de nuevos registros | Bajo | Alto | OB_01,OB_05 |  
 | **RNFS_03** | Patrones de seguridad | Medio | Alto | OB_01,OB_05 |  
 | **RNFS_04** | Protección frente a accesos no autorizados | Bajo | Alto | OB_05 |     
 | **RNFS_05** | Control de acceso | Bajo | Alto | OB_05 |  
 | **RNFS_06** | Credenciales de acceso | Medio | Alto | OB_05 |
 | **RNFS_07** | Registro en lista de seguridad | Medio | Alto | OB_05 |  
 | **RNFS_08** | Ataques por inyección de SQL | Alto | Alto | OB_01,OB_05 |  
 | **RNFS_09** | Codificación de contraseñas | Medio | Alto | OB_05 |      
 | **RNFO_01** | Aplicación en segundo plano | Alto | Alto | OB_01,OB_02 | 
 | **RNFO_02** | Tipos de formularios | Medio | Bajo | OB_02,OB_03,OB_12 | 

<br>

>	Matriz de trazabilidad de Restricciones Técnicas frente a Objetivos de Negocio.

 | **ID** | **Nombre** |  **Nivel de complejidad** | **Nivel de prioridad** | **Objetivos de Negocio** |
 | :--: | :----- |  :-----: | :-----: | :----- |
 | **RT_01** | Motor de la base de datos | Medio | Alto | OB_04 |  
 | **RT_02** | Código de la aplicación | Medio | Alto | OB_01 |  
 | **RT_03** | Formas geolocalización | Alto | Alto | OB_12,OB_13,OB_14 |    
 | **RT_04** | Intercambio de datos vía Internet | Medio | Alto | OB_01,OB_04,OB_05 |  
 | **RT_05** | Servidores | Medio | Alto | OB_04 |   
 | **RT_06** | Compatibilidad de SO | Alto | Alto | OB_01 |    
 
 <br>

>	Matriz de trazabilidad de Requisitos de Integración frente a Objetivos de Negocio.

| **ID** | **Nombre** | **Criterios de aceptación** | **Nivel de complejidad** | **Nivel de prioridad** | **Objetivos de Negocio** |
 | :--: | :----- | :-----: | :-----: | :-----: | :----- |
 | **RI_01** | Servicio @firma | Siempre que sea necesario usar la firma electrónica se usará el servicio @firma | Medio | Medio | OB_01,OB_03,OB_14 |
 | **RI_02** | Servicio 'Dni electrónico' | Se hará uso del Dni electrónico siempre que sea necesario verificar un DNI | Medio | Medio | OB_01,OB_03,OB_14 |
