* **Identifique las reglas de negocio.**


Una cámara de video control vial, mide la velocidad con la que los autos pasan por una calle. En la ciudad, se cuentan con *n* cantidad de cámaras. Cada cámara detecta automáticamente al vehículo cuando pasa y envía a nuestro sistema los siguientes datos: fecha y hora, id de la cámara, patente y velocidad. El paso de cada vehículo deberá registrarse en el sistema. Cada cámara tiene un id, una descripción, coordenadas x e y de su ubicación, dirección IP y modelo de la cámara. El sistema debe funcionar 24/7.

Cuando el sistema recibe los datos de un vehículo que pasó, el sistema realiza distintas acciones según la velocidad:

* si la velocidad es mayor a 70 km/h:  
  * el sistema envía los datos a una API que se encargará de guardarlos en una base de datos  
  * el sistema envía un correo con los datos que envió la cámara a la cuenta "avisos@ciudad"  
* si la velocidad es mayor a 100 km/h:  
  * el sistema envía los datos a una API que se encargará de guardarlos en una base de datos  
  * el sistema envía un correo con los datos que envió la cámara a la cuenta "alertas@ciudad"  
  * el sistema envía, 3 veces, los datos recibidos por la cámara a una impresora para que sean impresos


  

HECHO: Cada cámara tiene un ID.

RESTRICCIÓN: Cada cámara no debe enviar un registro si no pasa ningún vehículo.

ACCIÓN DISPARADORA: Medir la velocidad del vehículo, enviar fecha/hora, ID y patente cuando pase por la calle.

CÁLCULOS: La cantidad total de cámaras de la ciudad se calcula con la suma de la cantidad de ID, descripciones, coordenadas, direcciones IP y modelos proporcionados.

INFERENCIA: Si la cámara no detecta automáticamente los autos cuando pasan, esta defectuosa.