**ID:**\
CU-PR-3  

**Nombre:**\
Generar Reporte Parcial

**Autor:**\
Sandoval Bravo Alejandro

**Fecha de creación:**\
19 de marzo de 2020

**Fecha de actualización:**\
23 de mayo de 2020

**Descripción**\
El *Practicante* deberá poder generar su `PARTIAL REPORT` y registrar las `ACTIVITY` que haya realizado durante un tiempo determinado para que pueda ser consultado y calificado, posteriormente, por el maestro.

**Actor:**\
*Practicante*, *SPP*

**Precondiciones**\
PRE-1. Se encuentra un `PROJECT` vinculado a algún `PRACTITIONER`.

**Flujo Normal:**
  1. El *SPP* despliega la interfaz `View_GeneratePartialReport` mostrando etiquetas de texto que señalan la información que deberá ser ingresada (NRC, Periodo Escolar, Periodo del Reporte, Horas Cubiertas, Número de Informe; y de las `ACTIVITY`: Tiempo Real Empleado) en el campo de texto adyacente. Debajo del último campo de texto, se encuentran los botones `Añadir Actividad` y, al final de la ventana, dos botones `Generar` `Cancelar`.
  2. El `PRACTITIONER`, escribe la información solicitada por el *SPP* y da clic en el botón `Generar`.
  3. El *SPP* muestra un diálogo de alerta `Dialog_Confirmation`
  4. El `Practitioner` da clic en el botón "Sí".
  5. El *SPP* guarda el `PARTIAL REPORT` en la base de datos y cierra el diálogo de Alerta.

**Flujos Alternos:**
  1. *Cancelar Caso de Uso*
     1. El `PRACTITIONER` da clic al botón "Cancelar".
     2. El *SPP* termina la actividad y regresa a la interfaz `View_Project`.
  2. *Cancelar Confirmación*
     1. El `PRACTITIONER` da clic en el botón "No".
     2. El *SPP* cierra el diálogo de alerta y regresa al FN-2.
  3. *Añadir Actividad*
     1. El `PRACTITIONER` da clic en botón "Añadir Actividad".
     2. El *SPP* repetirá los campos de la información de la `ACTIVITY` para ingresar una nueva.

**Excepciones:**
   1. *Error al conectar con Base de Datos*
      1. El *SPP* no puede conectarse con la Base de Datos para guardar la `ACTIVITY`.
      2. El *SPP* muestra un diálogo de mensaje `Dialog_ConnectionError`.

**Postcondiciones:**\
Post-1. El `PARTIAL REPORT` se guardó exitosamente en la Base de Datos.

**Incluye (Relación Include):**\
No incluye.

**Extiende (Relación Extend):**\
No extiende.