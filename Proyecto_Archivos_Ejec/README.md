# Motor de Inferencia Lógica como Servicio

Este proyecto es un servicio web basado en lógica declarativa que actúa como un motor de inferencia simbólica. Permite ejecutar consultas lógicas sobre una base de conocimiento escrita en Prolog a través de una API REST. 

El sistema demuestra la integración de tres paradigmas de programación:
- *Programación lógica:* Reglas y hechos (Tau Prolog).
- *Programación funcional:* Normalización de datos (JavaScript).
- *Programación asíncrona:* Manejo de concurrencia y callbacks (Node.js y Express).

---

## ⚙️ Requisitos Previos

Para ejecutar este proyecto de manera local, asegúrate de tener instalado en tu sistema:
- [Node.js](https://nodejs.org/) (Versión LTS recomendada). Esto incluye el gestor de paquetes npm.

---

## 🛠️ Instalación Local

Sigue estos pasos para clonar e instalar las dependencias del proyecto en tu computadora:

1. *Clona el repositorio:*
   ```bash
   git clone <URL_DE_TU_REPOSITORIO>
   cd motor-inferencia
2. *Intalar las dependencias del Proyecto*
   Esto instalara *express* para el servidor HTTP y *tau-prolog* para el motor de inferencia.
    ```bash
    npm install
3. *Verifica los Archivos:*
   Asegurase que el archivo *knowledg.pl* este en la misma ruta que *index.js* antes de empezar.


# Instrucciones de Ejecucion
1. Ejecuta el siguiente comando en la raiz dle proyecto:
    ```bash
    node index.js
2. Realiza una consulta (Prueba de cliente)
   Con el servidor corriendo en la primera terminal, abre una nueva ventana/pestaña en tu terminal y ejecuta el siguiente comando cur1 para interactuar con la API:
*Consulta Verdadera:*
    ```bash
    curl-POST http://localhost:3000/query \
    -H "Content-Type: application/json" \
    -d '{"query": "penalty_applicable (contract1)."}'

    Consulta de Variables:
    curl-XPOSThttp://localhost:3000/query \
    -H "Content-Type: application/json" \
    -d '{"query": "penalty_applicable (X)."}'

3. Respuesta esperada
   El servidor responderá con un objeto JSON detallando el éxito de la consulta, la petición original y el resultado de la inferencia:
    ```bash
    {"success": true,
    "query": "penalty_applicable(contract1).",
    "results": [
    "true ;"
    }
