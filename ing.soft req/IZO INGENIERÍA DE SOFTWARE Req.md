IZO INGENIERÍA DE SOFTWARE

* **Identifique los requerimientos**.


Una cámara de video control vial, mide la velocidad con la que los autos pasan por una calle. En la ciudad, se cuentan con *n* cantidad de cámaras. Cada cámara detecta automáticamente al vehículo cuando pasa y envía a nuestro sistema los siguientes datos: fecha y hora, id de la cámara, patente y velocidad. El paso de cada vehículo deberá registrarse en el sistema. Cada cámara tiene un id, una descripción, coordenadas x e y de su ubicación, dirección IP y modelo de la cámara. El sistema debe funcionar 24/7.

REQUERIMIENTOS FUNCIONALES:

– El sistema debe permitir que cada cámara pueda registrar automáticamente el paso de cada vehículo.

– El sistema debe almacenar los datos de cada una de las cámaras para cada uno de los vehículos.

– Las cámaras deben detectar de forma automática a los vehículos que pasan por la calle.

– Cada una de las cámaras deben tener un ID, su  respectiva descripción, coordenadas tanto X como Y, una dirección IP y su modelo correspondiente.

REQUERIMIENTOS NO FUNCIONALES:

Disponibilidad: el sistema debe estar disponible en todo momento, 24/7.

Eficiencia: el sistema debe ser capaz de guardar los datos brindados por las cámaras en tiempo real, con demora casi nula.

Escalabilidad: El sistema debe tener la capacidad de poder manejar una cierta cantidad \`\`n\`\` de cámaras