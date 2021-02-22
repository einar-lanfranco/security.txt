# security.txt
Security.txt es un estándar propuesto [(ver Draft IETF)](https://tools.ietf.org/html/draft-foudil-securitytxt-10) que brinda a las organizaciones que publican servicios web definir políticas de seguridad. La implementación del archivo security.txt permite dar a conocer las pautas y canales de comunicación ante el hallazgo de vulnerabilidades.

[Consideraciones sobre el contenido]  
El archivo security.txt contiene una serie de campos a completar, algunos son de carácter obligatorio y otros opcionales.
> • Contact:  
> • Encryption:  
> •	Acknowledgments:  
> •	Canonical:  
> •	Policy:  
> •	Hiring:  

[Ejemplo]

```
Contact: mailto:cert@icic.gob.ar
Encryption: https://github.com/cert-ar/PGP-Key/blob/main/CERT-AR-PGP-2021.asc
Preferred-Languages: es, en
```
[Algunas consideraciones respecto a su uso]  
El archivo security.txt debe ser en texto plano y presentarse a través de HTTPS en una ubicación determinada.

[Referencias]  
• Sitio web del proyecto:  [https://securitytxt.org/](https://securitytxt.org/)
• Draft en IETF:  [https://tools.ietf.org/html/draft-foudil-securitytxt-10](https://tools.ietf.org/html/draft-foudil-securitytxt-10)
