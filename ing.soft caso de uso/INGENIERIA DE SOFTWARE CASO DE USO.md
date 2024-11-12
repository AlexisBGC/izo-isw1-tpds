* **Realice el caso de uso.**

Una cámara de video control vial, mide la velocidad con la que los autos pasan por una calle. En la ciudad, se cuentan con *n* cantidad de cámaras. Cada cámara detecta automáticamente al vehículo cuando pasa y envía a nuestro sistema los siguientes datos: fecha y hora, id de la cámara, patente y velocidad. El paso de cada vehículo deberá registrarse en el sistema. Cada cámara tiene un id, una descripción, coordenadas x e y de su ubicación, dirección IP y modelo de la cámara. El sistema debe funcionar 24/7.

Cuando el sistema recibe los datos de un vehículo que pasó, el sistema realiza distintas acciones según la velocidad:

* si la velocidad es mayor a 70 km/h:  
  * el sistema envía los datos a una API que se encargará de guardarlos en una base de datos  
  * el sistema envía un correo con los datos que envió la cámara a la cuenta "avisos@ciudad"  
* si la velocidad es mayor a 100 km/h:  
  * el sistema envía los datos a una API que se encargará de guardarlos en una base de datos  
  * el sistema envía un correo con los datos que envió la cámara a la cuenta "alertas@ciudad"  
  * el sistema envía, 3 veces, los datos recibidos por la cámara a una impresora para que sean impresos

ACTORES:  
   
**Principales**: Cámara  
**Secundarios**: API, sistema de correo, Impresora.  
**Precondiciones**: El sistema opera las 24/7 para una supervisión continua.

CASO DE USO:

1. **La cámara envía los datos al sistema.**  
2. **El sistema registra los datos proporcionados y los evalúa.**  
3. **Fin el caso de uso**

CAMINOS ALTERNATIVOS:

     **3.a La velocidad del vehículo es mayor a 70 km/h.**  
     **4.a El sistema envía los datos a una API.**  
     **5.a La API los guarda en una base de datos.**  
     **6.a  El sistema envía un correo con los datos a la cuenta “avisos@ciudad”.**  
     **7.a Fin de caso de uso**

—------------------------------------------------------------------------------------------------  
      **3.b  La velocidad del vehículo es mayor a 100 km/h.**

      **4.b El sistema envía los datos a una API.**  
      **5.b La API los guarda en una base de datos.**  
      **6.b El sistema envía un correo con los datos a la cuenta del sistema de correo “alerta@ciudad” y envìa 3 veces los datos a una impresora.**  
      **7.b La impresora imprime los datos recibidos.**  
      **8.b Fin de caso de uso.**

**ESCENARIO DE ÉXITO:**

1. **Se logra detectar y registrar correctamente.**

**ESCENARIO DE FRACASO:**

2. **Error en la detección.**  
3. **Error en el envío de datos.**  
4. **Error en la API.**  
5. **Problema con el envío del correo.**  
6. **Error en la impresión.**

### **Posibles Entidades en el DER**

1. **Cámara:**  
   * **Atributos: ID, descripción, coordenadas (x, y), dirección IP, modelo.**  
2. **Vehículo:**  
   * **Atributos: patente, modelo, marca.**  
3. **Registro de Velocidad:**  
   * **Atributos: fecha y hora, velocidad, ID de la cámara, ID del vehículo.**  
4. **Sistema (como entidad):**  
   * **Atributos: ID del sistema, estado (activo/inactivo), ubicación (servidor), etc. (si es relevante).**

### **Relaciones**

* **Cámara a Registro de Velocidad:**  
  * **Relación: Una cámara puede registrar múltiples velocidades (uno a muchos).**  
* **Vehículo a Registro de Velocidad:**  
  * **Relación: Un vehículo puede ser registrado múltiples veces (uno a muchos).**  
* **Sistema a Registro de Velocidad:**  
  * **Relación: El sistema gestiona los registros (uno a muchos, si decides incluir el sistema como entidad).**

### **Ejemplo de DER**

* **Cámara (1) — (N) Registro de Velocidad**  
* **Vehículo (1) — (N) Registro de Velocidad**  
* **Sistema (1) — (N) Registro de Velocidad (opcional)**

### **Conclusión**

**Incluir el sistema como una entidad en el DER es útil si deseas representar cómo se gestiona la información y las interacciones que tiene con otras entidades. Si el enfoque es más en las cámaras y los vehículos, podría no ser necesario. Depende del nivel de detalle que quieras alcanzar en tu modelo. Si necesitas más detalles sobre cómo estructurarlo, ¡avísame\!**

**4o mini**

