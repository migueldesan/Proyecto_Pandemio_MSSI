# 5. DESCRIPCIÓN DE LOS SUBSISTEMAS DEL SISTEMA A DESARROLLAR 

El proyecto a desarrrollar, Pandemio, va a tener distintas funcionalidades que completen los requisitos de la aplicación software, en esta sección se va a porceder a realizar una descripción detallada de los subsistemas a desarrollar dentro de la aplicación software.

|**SUB_01**| Gestor de localizaciones 
| :---: | :--- |
|**Dependencias**| Los objetivos de negocio de los que depende son: <br>+ OB_04 - Rastrear y gestionar la información de los usuarios de forma anónima. <br>+ OB_06 - Reducir el impacto de futuras pandemias en la sociedad. <br>+ OB_11 - Verificar que los usuarios cumplen las cuarentenas que deban hacer de forma automática. <br>+ OB_12 - Rastrear a los contactos estrechos de los usuarios. <br><br> Los procesos de negocio a implantar de los que depende son: <br> +PRI_02 - Establecer cuarentena y seguimiento. <br>+ PRI_03 - Rastrear contactos. <br>+ PRI_04 - Comprobar medidas sanitarias. <br>|
|**Descripción**| Subsistema encargado de localizar a los usuarios, ya sea por localización GPS o por triangulación por las antenas móviles
|**Importancia**| Alta
|**Prioridad**| Alta

|**SUB_02**| Gestor de notificaciones
| :---: | :--- |
|**Dependencias**| Los objetivos de negocio de los que depende son: <br>+OB_03 - Alcanzar el mayor número de población posible. <br>+ <br> + OB_07	Automatizar el proceso de citaciones para realizar pruebas médicas. <br>+ OB_08	Informar a los usuarios que deben acudir a realizarse pruebas médicas. <br>+ OB_09	Avisar a las fuerzas del orden si un usuario no acude a realizarse las pruebas médicas. <br>+ OB_10	Avisar a las fuerzas del orden si un usuario no cumple con la cuarentena que se le ha impuesto. <br>+ OB_11	Verificar que los usuarios cumplen las cuarentenas que deban hacer de forma automática. <br><br> Los procesos de negocio a implantar de los que depende son: <br>  + PRI-01 -  Realizar pruebas médicas <br>+ PRI-02 - Establecer cuarentena y seguimiento|
|**Descripción**| Este subsistema agrupa los requisitos relacionados con la notificación de avisos (cuarentena o cita médica) así como la gestión de formularios para avisar de casos positivos/sospechosos de personas.
|**Importancia**| Alta
|**Prioridad**| Alta

|**SUB_03**| Gestor de estadísticas
| :---: | :--- |
|**Versión**| 1.0
|**Dependencias**| 
|**Descripción**| Subsistema encargado de realizar estadísticas ¿y compartirlas?
|**Importancia**| Media
|**Prioridad**| Media

|**SUB_04**| Gestor general
| :---: | :--- |
|**Dependencias**|
|**Descripción**| Este subsistema agrupa los requisitos relacionados con la comunicación de los casos positivos entre CCAA (recordemos que la Sanidad está transferida a las CCAA y cada una de ellas tendrá su propia base de datos a las que no pueden acceder las demás) y a otros países; así como los cambios de dialecto y/o idioma (catalán, gallego, euskera, valenciano e inglés) dentro de la aplicación de Pandemio. 
|**Importancia**| Media
|**Prioridad**| Baja
|**Comentarios**| El número de personas que se desplacen entre comunidades o a otros países durante una futura pandemia será muy limitado como ha ocurrido en la actualidad. Además, aunque el español ahora no se considera lengua vehicular, la opción de poder cambiar de dialecto/idioma no se considera una prioridad.
Por estas dos razones se considera que este subsistema es de prioridad baja pero de importancia media. |

