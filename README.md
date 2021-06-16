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
#### Utilización
```bash
> ftp
ftp > open localhost port
ftp > open 0.0.0.0 2222
```
#### Default user
usuario: fernando
password: 1234

Con esta configuración, ya es posible transferir archivos PSV.

### Predicción de población:
Este servicio es capaz de determinar la población de personas en una generación, en base de una población de personas. Esto es posible mediante la implementación de un algoritmo genético. P (Población) será un arreglo "H", "M", "H", "M", "M"]
```bash
http://localhost:9595/examenfinal/ia?population=h,m,h,m,h,m&generation=10
```
#### Parámetros de entrada:
    'generation': 10

#### Respuesta 
    {
    "status": 200,
    "message": "Genetic Algorithm completed successfully",
    "populationDto": {
        "population": [
            "m",
            "m",
            "m",
            "m",
            "m",
            "m"
        ],
        "males": 0,
        "famales": 6
    }
}

### Controlador de actualización:
Este endpoint es capaz de cargar un archivo con extensión xls y xlsx, y generar un archivo
equivalente en formato XML. Este archivo se almacena en un tiempo de 5 minutos en un folder del sistema de archivos. Cuenta también con un proceso automático que verifica la los archivos en ese folder y elimina aquellos con más de 5 minutos almacenados.

```bash
POST http://<server>:<port>/examen-final/upload
```
#### Parámetros de entrada
    'a': 8,
    'b': 1'

### Response 
    {
	status: 200,
	message: "se ha almacenado el archivo"
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
