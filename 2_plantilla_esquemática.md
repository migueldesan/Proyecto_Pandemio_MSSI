# PRACTICA DE MODELADO
## 2 INFORMACIÓN DEL DOMINIO DEL PROBLEMA

Desde comienzos del año 2020 el mundo se encuntra sumergido en una pandemia global debido al virus COVID-19. Actualmente, en España, como modo de rastreo del virus y como ayuda a los ciudadanos, se ha creado sistemas software para intentar reducir los daños que está provocando la pandemia.

## 2.1 Introducción al Dominio del Problema

A pesar del uso de las aplicaciones de rastreo ya existentes nos encontramos con distintos problemas:
* El uso y la instalación de la aplicación no es obligatorio, lo cual dificulta el rastreo del virus y el poder avisar a la gente que ha estado en contacto con una persona que ha dado positivo.
* La aplicación está basada en el uso del Bluetooth y generalmente suele estar apagado u ocupado por otros dispositivos por lo que no funciona correctamente.
* Desconocimiento del uso de la aplicación y/o desconociento de uso de los dispositivos móviles. 
* El uso y almacenado de los datos del usuario debido a la Ley de protección de datos es complicado de manejar.
* Algunos ciudadanos incumplen la cuarentena obligatoria y no acuden a realizarse la prueba PCR o los test rápidos siendo contactos estrechos o presentando síntomas.


## 2.2 Glosario de Términos

A continuación se presenta una lista ordenada alfabétcamente con los principales términos, acrónimos y abreviaturas específicos del dominio del problema.

* **Aislamiento sanitario:** Lo llevan a cabo personas que están en su domicilio porque poseen confirmación médica de haber contraído COVID-19 o porque están esperando diagnóstico definitivo (caso sospechoso).

* **Aplanar la curva:** El objetivo para luchar contra el coronavirus es reducir el número de contagiados. La curva de la gráfica de contagio se aplana cuando deja de crecer el número de contagiados y se dibuja algo así como una 'meseta'. Es la forma gráfica de ver que durante un periodo de tiempo, el número de contagios se mantiene y no se incrementa, lo que significa que la velocidad de los contagios es menor y, por tanto, que se ha frenado la tendencia al alza.

* **Bluetooth:** Especificación industrial para redes inalámbricas de área personal (WPAN) creado por Bluetooth Special Interest Group, Inc. que posibilita la transmisión de voz y datos entre diferentes dispositivos mediante un enlace por radiofrecuencia en la banda ISM de los 2.4 GHz. Los principales objetivos que se pretenden conseguir con esta norma son:
  - Facilitar las comunicaciones entre equipos móviles.
  - Eliminar los cables y conectores entre estos. 
  - Ofrecer la posibilidad de crear pequeñas redes inalámbricas y facilitar la sincronización de datos entre equipos personales.
  
* **Caso sospechoso:** Cuadro clínico de infección respiratoria aguda de aparición súbita de cualquier gravedad que cursa, entre otros, con fiebre, tos o sensación de falta de aire. Otros síntomas atípicos como la odinofagia (dolor de garganta al ingerir), anosmia (pérdida de olfato), ageusia (pérdida de gusto), dolores musculares, diarreas, dolor torácico o cefaleas, entre otros, pueden ser también considerados como síntomas de sospecha de infección.

* **Contacto (estrecho):** Persona que haya coincidido con un caso diagnosticado como COVID positivo, permaneciendo a menos de 2 metros, durante más de 15 minutos, sin mascarilla y durante las 48 horas previas a la fecha del diagnóstico. Si se usaron mascarillas en todo momento, por parte tanto de estudiantes como profesores, se mantuvo la distancia de seguridad y las aulas estaban ventiladas, no se considerarían contactos estrechos.

* **Contagio:** Es la transmisión de una enfermedad por contacto con el agente patógeno que la causa. El coronavirus tiene un alcance de reproducción de 2,68 según la revista científica Lancet. Es decir, cada persona contagiada llega a contagiar a 2,68 personas, un índice relativamente alto, lo que ha facilitado su expansión por el mundo.

* **Coronavirus:** Son una gran familia de virus que pueden provocar enfermedades tanto a animales como a humanos. Se sabe que, en los humanos, todos los virus de esta familia pueden causar infecciones respiratorias, que pueden ir desde un resfriado normal a una enfermedad grave, como son la SRAS, la MERS o el Covid-19. La primera vez que se habló de este tipo de virus fue en la revista Nature el 16 de noviembre de 1968. Los investigadores lo llamaron 'coronavirus' porque la forma del virus al microscopio era como similar al de la corona solar.

* **COVID-19:** Enfermedad infecciosa causada por el coronavirus SARS-CoV-2 que se ha descubierto más recientemente. El origen léxico del Covid-19 proviene de 'co', en alusión la forma de corona solar del virus, 'vi' corresponde a la palabra virus y 'd' hace referencia a enfermedad ("disease" en inglés). Finalmente se le puso el número 19 por el año en que se detectó en seres humanos.

* **Cuadro clínico:** Conjunto de signos y síntomas con presentaciones leves como fiebre y tos, malestar general, dolor de garganta, mucosidad, asociados o no, a síntomas graves como dificultad respiratoria o neumonía. Pueden presentarse como neumonía intersticial y/o con compromiso del espacio alveolar.

* **Cuarentena:** Se trata de un aislamiento preventivo durante un tiempo determinado con el objetivo de evitar el contagio de ciertas enfermedades. No tienen por qué ser 40 días exactos. De hecho, para este coronavirus suele rondar los 10 días.

* **Estado de alarma:** En España, se declara en todo el país (o en parte de este) mediante un decreto del consejo de ministros en el caso de calamidades, desgracias públicas como inundaciones, terremotos o crisis sanitarias como la que vivimos por culpa del coronavirus. Esta disposición permite limitar la libre circulación de las personas, intervenir industrias, requisar temporalmente bienes, y limitar o racionar los servicios o el consumo de artículos de primera necesidad.

* **Incubación:** Se trata del tiempo comprendido entre la exposición a un organismo patogénico y el momento en que los síntomas aparecen por primera vez. En el caso del coronavirus, el tiempo de incubación es de 5,4 días de media, aunque se han observado casos en que el periodo de incubación es de hasta 14 días.

* **Pandemia:** Tal y como establece la OMS, se llama pandemia a la propagación a gran velocidad y a escala mundial de una nueva enfermedad. Lo que la diferencia de la epidemia es el grado en que aumentan los casos y su alcance internacional. La OMS declaró la pandemia cuando el coronavirus se extendió por los seis continentes y se certificaron contagios en más de 100 países de todo el planeta.

<img align="right" width=50% src="./Imágenes/PCR7.jpg">

* **PCR:** La reacción en cadena de la polimerasa, conocida como PCR por sus siglas en inglés (polymerase chain reaction), es una técnica de la biología molecular desarrollada en 1986 por Kary Mullis. Su objetivo es obtener un gran número de copias de un fragmento de ADN particular, partiendo de un mínimo; en teoría basta partir de una sola copia de ese fragmento original, o molde. En alguno casos, como en la actual epidemia de coronavirus SARS-CoV-2, se están empleando las PCR para detectar, confirmar o descartar la presencia del coronavirus en el organismo, ya que esta prueba de diagnóstico permite localizar y ampificar un fragmento del material genético de un patógeno o microorganismo, que en el caso del coronavirus es una molécula de ARN. El Ministerio de Sanidad subraya en el documento de Estrategia de detección precoz, vigilancia y control del Covid-19 que las muestras recomendadas para la PCR son del tracto respiratorio superior e inferior:
  - Superior: exudado preferiblemente nasofaríngeo y orofaríngeo o exudado nasofaríngeo. 
  - Inferior: preferiblemente lavado broncoalveolar, broncoaspirado, esputo (si es posible) y/o aspirado endotraqueal, especialmente en pacientes con enfermedad respiratoria grave. 
  
  Así, la toma de la muestra se obtiene inclinando ligeramente la cabeza del paciente hacia atrás, se introduce un hisopo o bastoncillo en la garganta, hasta la faringe, y se rota o da vueltas de cinco a 10 segundos, aunque también se puede tomar la muestra del interior de la nariz, por lo que se introduce el bastoncillo por un orificio nasal unos cinco o siete centímetros hasta la nasofaringe y se gira durante unos segundos para obtener el tejido necesario.

* **Test rápido:** Este nuevo test rápido de antígeno es una nueva prueba de la que disponemos que nos permite detectar el virus desde el mismo inicio del contacto con una altísima fiabilidad, muy similar a la que nos ofrecerá una PCR, pero con obtención de resultados en apenas 15 minutos. Los test rápidos  se realizan con muestras de exudados de la nariz y del fondo de la garganta –que se toman con un bastoncillo o hisopo– y en ellos se detectan la posible presencia de antígenos, es decir, permiten detectar si hay presencia del virus SARS-CoV-2 em el paciente por medio de alguno de sus componentes, como por ejemplo, por sus proteínas.

> En la siguiente imagen podemos ver las principales diferencias entre la técnica de la PCR y los test rápidos.

* **Vacuna:** Se trata de una sustancia compuesta por microorganismos atenuados o muertos que se introduce para estimular la formación de anticuerpos y conseguir inmunidad frente a ciertas enfermedades. Hasta la fecha no existe ninguna vacuna ni medicamento antiviral específico para prevenir o tratar el Covid-19.
