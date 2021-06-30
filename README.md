# Security.txt
*Security.txt* es un estándar propuesto [(ver Draft IETF)](https://tools.ietf.org/html/draft-foudil-securitytxt-11) que brinda a las organizaciones que publican servicios web definir políticas de seguridad. El estándar define la implementación de un archivo de texto, *security.txt*, cuyo contenido permite dar a conocer las pautas y canales de comunicación ante el hallazgo de vulnerabilidades.  
  
  
**[Consideraciones sobre el contenido]**  
  
El archivo *security.txt* contiene una serie de campos a completar, algunos son de carácter obligatorio y otros opcionales.
> • *Contact*:  Campo de carácter requerido, se indica cual será el canal de contacto a utilizar para comunicarse con la organización. Se sugiere indicar una dirección de correo del área de seguridad de la información. Si se indica una URL, el enlace deber comenzar con *https://* y *mailto:* para cuentas de correo.  
> 
> • *Expires*:  Campo de carácter requerido, se indica la fecha de caducidad del archivo, permite que el mismo sea sometido a revisión y actualización.  
> El formato empleado es *day-of-week, DD MM YYYY hh:mm zone*  
> 
> • *Encryption*: (Opcional). Se utiliza para indicar que se encuentra disponible la clave PGP para entablar comunicaciones cifradas. Las claves NO deben aparecer en este campo sino que se indicará la ubicación donde se puede recuperar la clave.  
> 
> •	*Acknowledgments*: (Opcional). La iniciativa permite indicar mediante un enlace el reconocimiento que realiza la organización a aquellas personas u organizaciones que han colaborado anteriormente con informes de seguridad.  
> 
> •	*Preferred-Languages*: (Opcional). Este campo se puede utilizar para indicar un conjunto de lenguajes naturales que se prefieren para recibir información. Este conjunto puede listar varios valores, separados por comas. Si este campo está incluido, debe indicarse al menos un valor. Los valores dentro de este conjunto son etiquetas de idioma compuestos por las dos letras iniciales del mismo.  
> 
> • *Canonical*: (Opcional). Este campo se utiliza para indicar la ubicación donde se encuentra el archivo security.txt.  
> 
> •	*Policy*: (Opcional). Este campo permite especificar un enlace donde se encuentra la política de seguridad sobre la divulgación de vulnerabilidades de la organización.  
> 
> •	*Hiring*: (Opcional). Se puede utilizar este campo para indicar, a través de un enlace, posiciones de trabajo de la organización relacionadas con seguridad.  
  
  
**[Ejemplo]**
  
```
Contact: mailto:reportes@cert.ar
Expires: Fri, 31 Dec 2021 23:00 -0300
Encryption: https://github.com/cert-ar/PGP-Key/blob/main/CERT-AR-PGP-2021.asc
Preferred-Languages: es, en
Canonical: https://github.com/cert-ar/security.txt/blob/main/security.txt
```
Puede descargar nuestro ejemplo [Aquí](https://github.com/cert-ar/security.txt/blob/main/security.txt)
  
  

**[Algunas consideraciones respecto a su uso]**  

El archivo *security.txt* debe ser en texto plano y presentarse a través de HTTPS en una ubicación determinada.  
•	Sitios web: El archivo security.txt debe colocarse en la ruta /.well-known/security.txt
> En caso de no ser posible utilizar el directorio /.well-known/ se recomienda utilizar la raíz del directorio como ubicación del archivo.  
> 
•	Repositorios: El archivo debe ubicarse en la raíz del repositorio.  
Cuando en uno de los campos se indica una URL, el enlace deber comenzar con *https://*  
  
  
**[Importante]**

La presencia del archivo *security.txt* **no** debe ser considerada como un permiso para la ejecución de pruebas o análisis.
Se sugiere revisar la correcta utilización del campo *Policy* y la divulgación de vulnerabilidades, puede leer más en el apartado [3.5.7](https://tools.ietf.org/html/draft-foudil-securitytxt-11#section-3.5.7); y en particular el apartado [6.5](https://tools.ietf.org/html/draft-foudil-securitytxt-11#section-6.5) del estándar.

**[Ventajas ante otras propuestas]**

Una ventaja importante del uso de este mecanismo ante alternativas como, por ejemplo, la presentación de formularios de contacto o de páginas especiales que indiquen como contactarse es que no es necesario modificar de forma alguna el sitio web objetivo. Al ser este mecanismo es complementario, que consiste sólo en incluir un txt, el esfuerzo necesario para implementar y mantener esta solución en cualquier sitio web resulta insignificante sin importar la complejidad o las tecnologías utilizadas en ellos.


**[Referencias]**  
• Sitio web del proyecto:  [https://securitytxt.org/](https://securitytxt.org/)  
• Draft en IETF:  [https://tools.ietf.org/html/draft-foudil-securitytxt-11](https://tools.ietf.org/html/draft-foudil-securitytxt-10)
