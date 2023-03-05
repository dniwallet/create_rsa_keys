# Crear un par de claves RSA
Plantilla para crear un par de claves RSA de 4096 bits

```sh
# Generación del par RSA de 4086 bits
> openssl genrsa -out rsakey.pem 4096 

# Extracción de la clave publica del par RSA
> openssl rsa -in rsakey.pem -outform PEM -pubout -out pukey_proyecto.pem 

# Extracción de la clave privada del par RSA
> openssl rsa -in rsakey.pem -outform PEM -out prkey_proyecto.pem 

# Convertir la clave privada del par RSA a formato PKCS8
> openssl pkcs8 -topk8 -nocrypt -in prkey_proyecto.pem > prkey_proyecto_pkcs8.pem  
