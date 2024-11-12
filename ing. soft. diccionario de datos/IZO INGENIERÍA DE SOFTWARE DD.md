IZO INGENIERÍA DE SOFTWARE

* **Confeccione el diccionario de datos**.


Una cámara de video control vial, mide la velocidad con la que los autos pasan por una calle. En la ciudad, se cuentan con *n* cantidad de cámaras. Cada cámara detecta automáticamente al vehículo cuando pasa y envía a nuestro sistema los siguientes datos: fecha y hora, id de la cámara, patente y velocidad. El paso de cada vehículo deberá registrarse en el sistema. Cada cámara tiene un id, una descripción, coordenadas x e y de su ubicación, dirección IP y modelo de la cámara. El sistema debe funcionar 24/7.  
Cuando el sistema recibe los datos de un vehículo que pasó, el sistema realiza distintas acciones según la velocidad:

* si la velocidad es mayor a 70 km/h:  
  * el sistema envía los datos a una API que se encargará de guardarlos en una base de datos  
  * el sistema envía un correo con los datos que envió la cámara a la cuenta "avisos@ciudad"  
* si la velocidad es mayor a 100 km/h:  
  * el sistema envía los datos a una API que se encargará de guardarlos en una base de datos  
  * el sistema envía un correo con los datos que envió la cámara a la cuenta "alertas@ciudad"  
  * el sistema envía, 3 veces, los datos recibidos por la cámara a una impresora para que sean impresos

**DICCIONARIO DE DATOS:**

Cámara \= ID \+ descripcion \+ coordenadas x \+ coordenadas y \+ dirección IP \+ modelo

DatosReg \= fecha/hora \+ IDcámara \+ patente \+ velocidad

| Nombre  | Descripción | Longitud | Tipo | Dominio |
| :---- | :---- | :---- | :---- | :---- |
| IDcamara | identificador de la cámara | 30 | string |  |
| Desc.camara | descripción de la cámara (función,etc) | 100 | text |  |
| DIPcamara | dirección IP de la cámara | 30 | string |  |
| modelo | modelo de la cámara | 60 | text |  |
| coordenadas x | coordenadas de la ubicación x | 20 | float |  |
| coordenadas y | coordenadas de la ubicación y | 20 | float |  |
| fecha/hora | fecha y la hora de la detección del vehículo | 15 | datetime |  |
| patente | patente del vehículo | 15 | varchar |  |
| velocidad | velocidad en la que pasó el vehículo | 5 | decimal |  |

