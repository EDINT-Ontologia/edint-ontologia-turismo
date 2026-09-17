# Ontología EDINT Turismo (EDINT Tourism Ontology)
Este repositorio demuestra cómo se puede reutilizar la ontología de turismo que se está desarrollando en el contexto del espacio de datos de turismo promovido por SEGITTUR. Específicamente, se utilizan en los ejemplos las siguientes clases y propiedades:
## Clase AccomodationEstablishment
Los tipos de alojamiento son subclases: Hotel, Hostal, Hostel, Aparthotel, Vacation Rentals.
### Propiedades:
- accomodationRating (object property) entre AccomodationEstablishment y Rating
- numberOfAccomodationUnits (data property) xsd:int
- numberOfBeds (data property) xsd:int
- registrationNumber es identificador(data property) string
- hasDescription (object property) entre TourismEntity (superclase) y Description
- name (data property) xsd:string
- hasLocation (object property) entre Place (superclase) y Location 
- hasContactPoint (object property) entre Place (superclase) y ContactPoint

## Clase ContactPoint
### Propiedades:
- email (data property) xsd:string
- telephone (data property) xsd:string
- url (data property) xsd:string

## Clase Rating
### Propiedades:
- ratingUnit (data property) xsd:string. por ejemplo "stars"
- ratingValue (data property) xsd:string. por ejemplo "3"

## Clase Description
### Propiedades:
- longDescription (data property) xsd:string
- shortDescription (data property) xsd:string

## Clase Location
### Propiedades:
- autonomousCommunity (data property) xsd:string
- country (data property) xsd:string
- county (data property) xsd:string (comarca)
- province (data property) xsd:string
- locality (data property) xsd:string
- postal code (data property) xsd:string
- street address (data property) xsd:string 
- gsp:lat y gsp:long (subclase de gsp:Feature)

## Clase: HistoricalOrCulturalResource
Los tipos de recurso histórico-cultural son subclases: Alcazar, Amphiteatre, Acueduct, etc.

### Propiedades:
- name (data property) xsd:string
- hasLocation (object property) entre Place (superclase) y Location 
- hasDescription: (object property) entre TourismEntity (superclase) y Description

# Propósito y alcance de la ontología (Purpose and scope of the ontology)

El propósito de esta ontología es el de proporcionar un vocabulario común para la representación de las entidades y datos principales de los alojamientos y puntos de interés turísticos de una entidad local, para que luego se pueda realizar su explotación directamente en algún portal de turismo, o de manera agregada mediante los cubos de datos de turismo que se han definido para EDINT. Su alcance cubre los datos que pueden ser utilizados con los propósitos de conocer y gestionar el turismo dentro de la entidad local, que es parte de las funciones habituales de las entidades locales.

# Prefijo y espacio de nombres (Prefix and namespace)

El prefijo de la ontología es: `estur` y se encuentra publicada en el espacio de nombres: [https://ontologia.segittur.es/turismo/def/core#)](https://ontologia.segittur.es/turismo/def/core#)

# Estructura del repositorio (Repository structure)

El repositorio contiene las siguientes carpetas

| Carpeta | Descripción |
|--------|--------------|
| **examples/** | Contiene las fuentes de datos y los ejemplos en RDF generados con la ontología a partir de estas fuentes. |
| **mappings/** | Contiene los ficheros de los mappings (reglas de correspondencia) utilizados para generar los ejemplos en RDF.  |

# Mantenimiento y evolución (Maintenance and evolution)

Para manejar las incidencias o mejoras sugeridas con respecto a la ontología, recomendamos seguir las guías proporcionadas en ([Issues Management](./ISSUES.md)) para generar una incidencia.

# Financiación (Funding)

Los ejemplos aportados para el uso de esta ontología han sido desarrollados en el contexto del Espacio de Datos para las Infraestructuras Urbanas Inteligentes ([EDINT](https://edint.es)). El desarrollo de la ontología se está realizando en el contexto del espacio de datos de turismo anteriormente mencionado.

![Logos](./resources/EDINT_UE_V-Color.png)
