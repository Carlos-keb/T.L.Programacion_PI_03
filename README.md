# PROYECTO T.L_PROGRAMACION 
En este repsitorio se alojara todo lo relacionado al Proyecto Final " Motor de Inferencia Lógica como Servicio"

# Descrpcion General
El proyecto consiste en el diseño e implementación de un servicio web basado en lógica declarativa, el cual permite ejecutar consultas sobre una base de conocimiento escrita en Prolog a través de una API REST desarrollada en Node.js con Express.

El sistema actúa como un motor de inferencia simbólica, donde el usuario puede enviar consultas lógicas y recibir resultados derivados mediante reglas declarativas, integrando paradigmas de programación fundamentales estudiados en la materia.

# Objetivo
Desarrollar un sistema que demuestre la interacción entre distintos paradigmas de programación, específicamente:

- Programación lógica (Prolog)
- Programación funcional (JavaScript)
- Programación asíncrona (modelo de ejecución de Node.js)
- El sistema permitirá evaluar consultas sobre hechos y reglas definidas en una base de - conocimiento, retornando resultados inferidos de manera automática.

# Arquitectura del Sistema
El sistema está compuesto por un único módulo que integra:

- ***Servidor HTTP (Express)***
 - Exponer un endpoint /query
 - Recibe consultas en formato Prolog
- ***Motor de inferencia lógica***
  - Implementado mediante la biblioteca Tau Prolog
  - Evalúa reglas y hechos definidos en una base de conocimiento
- ***Base de conocimiento***
 - Archivo en Prolog con:
   - Hechos
   - Reglas
 - Define relaciones lógicas y condiciones de inferencia
- ***Capa asíncrona***
Maneja múltiples solicitudes concurrentes
Usa async/await y Promises

# Flujo de ejecución
***1- El cliente envía una consulta lógica (ej. penalty_applicable(contract1).)***
***2- El servidor:***
 - Normaliza la entrada (programación funcional)
 - Carga la base de conocimiento
 - Inicializa una sesión Prolog
 
***3- El motor lógico:***
 - Ejecuta la consulta
 - Realiza inferencia basada en reglas
 
***4- El resultado:***
Es retornado al cliente como respuesta JSON


# Colaboradores Del Protecto
- ***Keb Zi Jose Carlos***
- ***Bolaños Marin Gabriel Emilo***
- ***Pech Sanchez Jorge Armando***

Esperamos que este proyecto sea de su agrado :)
