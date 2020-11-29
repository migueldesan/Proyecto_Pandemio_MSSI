5. DESCRIPCIÓN DE LOS SUBSISTEMAS DEL SISTEMA A DESARROLLAR 

El proyecto a desarrrollar, Pandemio, va a tener distintas funcionalidades que completen los requisitos de la aplicación software, en esta sección se va a porceder a realizar una descripción detallada de los subsistemas a desarrollar dentro de la aplicación software.

|**SUB_01**| Gestor de localizaciones 
| :---: | :--- |
|**Versión**| 1.0
|**Dependencias**|  - Los procesos de negocio a implantar son:<br>+ PRI_03	Rastrear contactos <br>+Comprobar medidas sanitarias <br>-Los objetivos de negocio de los que depende son: <br>+OB_04	Rastrear y gestionar la información de los usuarios de forma anónima. <br>+ OB_06	Reducir el impacto de futuras pandemias en la sociedad. <br>+ OB_10	Avisar a las fuerzas del orden si un usuario no cumple con la cuarentena que se le ha impuesto. <br>+ OB_11	Verificar que los usuarios cumplen las cuarentenas que deban hacer de forma automática <br>+ OB_13	Mostrar un mapa de calor con las zonas de movilidad de los casos positivo
|**Descripción**| Subsistema encargado de localizar a los usuarios, ya sea por localización GPS o por triangulación por las antenas móviles
|**Importancia**| Alta
|**Prioridad**| Alta

|**SUB_02**| Gestor de notificaciones
| :---: | :--- |
|**Versión**| 1.0
|**Dependencias**| - Los procesos de negocio a implantar son <br>  + PRI-01 Realizar pruebas médicas <br>+ Establecer cuarentena y seguimiento <br>-Los objetivos de negocio de los que depende son: <br>+ OB_05	Preservar la privacidad de los usuarios. <br>+ OB_07	Automatizar el proceso de citaciones para realizar pruebas médicas. <br>+ OB_08	Informar a los usuarios que deben acudir a realizarse pruebas médicas. <br>+ OB_09	Avisar a las fuerzas del orden si un usuario no acude a realizarse las pruebas médicas. <br>+ OB_10	Avisar a las fuerzas del orden si un usuario no cumple con la cuarentena que se le ha impuesto. <br>+ OB_11	Verificar que los usuarios cumplen las cuarentenas que deban hacer de forma automática.
|**Descripción**| Subsistema encargado de notificar a los usuarios de avisar a los usuarios de que deben cumplir cuarentena o tienen citas médicas
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
|**Versión**| 1.0
|**Dependencias**|
|**Descripción**| Subsistema encargado de compartir los casos positivos entre comunidades y entre paises, y la gestión de idiomas
|**Importancia**| Media
|**Prioridad**| Baja
