# PRÁCTICA DE MODELADO
# 1 INTRODUCCIÓN
A finales de diciembre de 2019 se identificaron en Wuhan, en la provincia china de Hubei, 41 casos de neumonía. Un análisis más exhaustivo mostró que se trataba de un nuevo caso de coronavirus que fue denominado SARS-CoV-2 o como comúnmente se conoce Covid-19.

Cuando se detectaron los primeros casos, nadie podía imaginar que, unos meses más tarde, concretamente el 11 de marzo de 2020, la Organización Mundial de la Salud (OMS) declarará que el nuevo brote de coronavirus constituía una pandemia debido a que esta nueva enfermedad ya estaba presente en los seis continentes del planeta.

Actualmente hay más de 50 millones de casos confirmados en todo el planeta (y más de un millón de muertos relacionados con esta enfermedad) por lo que los países han tenido que tomar diferentes medidas para intentar aplanar la curva de incidencia del virus y evitar su rápida propagación como los cierres de fronteras o el confinamiento de la población. 

Además, ahora que se van conociendo más detalles de esta nueva enfermedad: cómo se propaga, cómo podemos reducir el número de contagios, síntomas relacionados, etc., están surgiendo diferentes sistemas software, como Radar Covid, para rastrear y gestionar la información de los ciudadanos con el fin de aplanar la curva de incidencia e intentar erradicar esta pandemia o posibles pandemias que surjan en el futuro. 

Sin embargo, ninguna de las aplicaciones actuales está teniendo los resultados que se esperaban ya que ninguna es obligatoria o se basan en software que no toda la población conoce, y por este motivo nace la aplicación de Pandemio.

Pandemio será una plataforma que permitirá rastrear y gestionar la información de los ciudadanos de la próxima pandemia con el fin de reducir el impacto de una enfermedad en la población y evitar tomar decisiones extremas como el confinamiento domiciliario de la población.

En este documento se especifican los aspectos más destacados de Pandemio, confiando en que sirvan como punto de partida para llevar a cabo el análisis detallado de los requisitos de este proyecto. Esta especificación de requisitos debe ser suficientemente precisa como para afrontar, en fases posteriores, el diseño y la implementación del proyecto.

<br>

### 1.1 Alcance
Dado que lo que se busca con esta aplicación es el control total sobre el contagio y expansión de la pandemia, se buscará alcanzar al máximo de la población posible, en este caso el 100% de las personas que utilizan smartphones.

Deberemos para ello llevar un proceso judicial con el objetivo de que Pandemio sea instalada en todos los smartphones de forma obligatoria, ya sea a través de Google en los Android o Apple en dispositivos iOS.

Una vez tengamos la certeza de que la aplicación está instalada en todos los smarthpones, el objetivo es controlar los contactos de las personas positivas en COVID-19 y los posibles contagios a través de la ubicación del teléfono o, en su defecto, por medio de una triangulación a través de las antenas de telefonía móvil. 

Por otro lado, habrá que considerar la posibilidad de que un positivo en COVID-19 o un contacto estrecho se desplace entre comunidades autónomas o incluso a otros países. La aplicación tendrá bases de datos independientes para cada comunidad autónoma, por lo que en caso de que se produzca un desplazamiento de este tipo se deberá advertir a los sistemas sanitarios de aquellos lugares en los que se les haya ubicado. En caso de permanecer en España podremos seguirles a través de Pandemio, pero de salir a otro país se daría aviso a sus autoridades sanitarias y pasaría a ser su responsabilidad.

Surge también el problema en cuanto al rastreo de personas que no utilizan smartphone. Tenemos que aceptar este hecho, intentando tener cierto seguimiento a través de sus familiares o personas cercanas y con ayuda del cuerpo sanitario, que deberá tener mayor control sobre este nicho de la población.

Siendo conscientes de que el rastreo de la ubicación y los movimientos de la población puede verse como una invasión a su intimidad, nos comprometemos a respetar en todo momento la Ley de Protección de Datos.

En cuanto al mantenimiento y actualizaciones de la aplicación, el objetivo inicial es obtener un producto final, aunque estaría abierto a versiones y actualizaciones en caso de necesidad.

<br>

### 1.2 Objetivos
En la siguiente tabla se describen los principales objetivos que se esperan alcanzar de Pandemio cuando se termine de implementar:
 | ID | OBJETIVO |
 | :--: | :----- |
 | **OB-01** | Mejorar las aplicaciones existentes en la lucha contra enfermedades. |
 | **OB-02** | Alcanzar el 100% de la población que disponga de dispositivos móviles. |
 | **OB-03** | Alcanzar el mayor número de población posible. |
 | **OB-04** | Rastrear y gestionar la información de los ciudadanos de forma anónima. |
 | **OB-05** | Preservar la privacidad de los ciudadanos. |
 | **OB-06** | Reducir el impacto de futuras pandemias en la sociedad. |
 | **OB-07** | Automatizar el proceso de citaciones para realizar pruebas médicas. |
 | **OB-08** | Informar a los ciudadanos que deben acudir a realizarse pruebas médicas. |
 | **OB-09** | Coordinar los diferentes servicios sanitarios y autoritarios de las distintas comunidades autónomas. |
 | **OB-10** | Verificar que los ciudadanos cumplan las cuarentenas que deban hacer. |
 | **OB-11** | Rastrear a los contactos estrechos de los ciudadanos. |
