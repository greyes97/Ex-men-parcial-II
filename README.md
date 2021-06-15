# EXAMEN FINAL INGENIERÍA DE SOFTWARE 2021

## Requerimientos: 
Para poder crear y construir la aplicación, necesita:
- [JDK 11](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
- [Maven 3](https://maven.apache.org)

## Proceso para clonar e iniciar el proyecto:
Para iniciar un nuevo proyecto usando Spring Boot, clone este repositorio en un nuevo directorio:

```bash
git clone https://gitlab.com/prejects-edfern/is-final-2021.git
```
Para construir la aplicación para producción, ejecute:
```bash
mvn package
```
## Funcionalidad del proyecto:

### Servicio FTP:
En este servicio se podrá subir un archivo en formato PSV, el cual cada minuto leerá los archivos 
alojados en el folder FTP y generará un archivo en formato JSON, en otro folder del FTP.

#### Params
    'a': 8,
    'b': 1'

### Response 
    HTTP/1.1 200 OK
    Date: Thu, 24 Feb 2011 12:36:30 GMT
    Status: 200 OK
    Connection: close
    Content-Type: application/json
    Content-Length: 2
    
    {
        "status": 200,
        "message": "success",
        "result": 9.0
    }
### Subtraction
`GET /math/sub 
`
```bash
http://localhost:8080/math/sub?a=8&b=1
```
#### Params
    'a': 8,
    'b': 1'

### Response 
    HTTP/1.1 200 OK
    Date: Thu, 24 Feb 2011 12:36:30 GMT
    Status: 200 OK
    Connection: close
    Content-Type: application/json
    Content-Length: 2
    
    {
        "status": 200,
        "message": "success",
        "result": 7.0
    }

### Multiplication
`GET /math/mul 
`
```bash
http://localhost:8080/math/mul?a=8&b=1
```
#### Params
    'a': 8,
    'b': 1'

### Response 
    HTTP/1.1 200 OK
    Date: Thu, 24 Feb 2011 12:36:30 GMT
    Status: 200 OK
    Connection: close
    Content-Type: application/json
    Content-Length: 2
    
    {
        "status": 200,
        "message": "success",
        "result": 8.0
    }

### Division
`GET /math/div 
`
```bash
http://localhost:8080/math/div?a=8&b=2
```
#### Params
    'a': 8,
    'b': 2'

### Response 
    HTTP/1.1 200 OK
    Date: Thu, 24 Feb 2011 12:36:30 GMT
    Status: 200 OK
    Connection: close
    Content-Type: application/json
    Content-Length: 2
    
    {
        "status": 200,
        "message": "success",
        "result": 4.0
    }

## Diagrama de clases
![alt text](doc/Math.png)
