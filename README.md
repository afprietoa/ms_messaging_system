# Messaging System Microservice

# Used Technologies
- Java version 11
- JUnit version 4.13.1
- Maven version 2.4.1
- Spring Boot version 2.7.11-SNAPSHOT

# Business problem
It's required to automate the merchandise shipments for tracking and updating them. 

The System will have several entities, customer, employee, packet and shipment

A customer is defined by:
- id card number
- first name
- last name
- cellphone
- e-mail
- address
- city

An employee is defined by:
- id card number
- first name
- last name
- cellphone
- e-mail
- city
- antiquity
- blood type
- employee type

A packet is defined by:
- code
- packet type
- weight
- declared value

A shipment is defined by
-  guide number
- origin city
- destiny city
- destiny address
- recipient name
- recipient contact
- delivery hour
- shipment state
- shipment costs

# Microservice proposal

REST API allows performing the next functionalities

1. A customer can register in the messaging database, in this ENDPOINT it is validated that the id card number is an integer, and the first and last name contain data, and these can´t be null.

Customer register, request customer ENDPOINT example (http://localhost:8080/api/v1/customer ) [POST]

Request Body

```json
{
    "cedula": 12345,
    "nombre":"Mateo",
    "Apellido":"Zapata",
    "celular": 3046303886
    "correoElectronico" : "mateo@gmail.com"
    "direccionResidencia" :"calle 46 # 69-90"
    "ciudad" : "Medellin"
}

```

Response Data

```java {.highlight .highlight-source-java .bg-black}
{
    "cedula": 12345,
    "nombre":"Mateo",
    "Apellido":"Zapata",
    "celular": 3046303886
    "correoElectronico" : "mateo@gmail.com"
    "direccionResidencia" :"calle 46 # 69-90"
    "ciudad" : "Medellin",
    "shipments": null
}

```