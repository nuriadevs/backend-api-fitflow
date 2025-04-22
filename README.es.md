# Backend - FitFlow App

## Descripción general

**FitFlow App** es un agente impulsado por IA que ayuda a los usuarios a descubrir y recibir recomendaciones de entrenamiento personalizadas. Utiliza una arquitectura RAG (Generación Aumentada por Recuperación) junto con **Upstash** para optimizar el almacenamiento y la recuperación semántica de entrenamientos.

El backend está construido con **TypeScript** y **Node.js**, y se conecta con una base de datos **MongoDB** para gestionar perfiles de usuario y datos de entrenamiento. Integra la API de **OpenAI** para ofrecer un asistente conversacional para las interacciones con el usuario.

## Tecnologías

- **Node.js**: Entorno de ejecución para JavaScript.
- **TypeScript**: Lenguaje basado en JavaScript.
- **MongoDB**: Base de datos NoSQL para almacenar usuarios y ejercicios.
- **Upstash**: Base de datos vectorial basada en RAG para búsqueda semántica rápida.
- **OpenAI API**: Clave API para usar el chat y consultar datos.
- **Jest**: Framework de pruebas para el backend y lógica de rutas.

## Funcionalidades principales

- **Autenticación**: Gestión de usuarios con JWT.
- **Recomendaciones de ejercicios**: Búsqueda y sugerencias personalizadas.
- **Asistente IA**: Interacción en lenguaje natural para guiar entrenamientos, guardados directamente en el perfil del usuario.
- **Integración RAG**: Usa Upstash para optimizar velocidad y precisión en consultas de ejercicios.

## Estructura del proyecto

````
backend/ 
├── docs/ # Documentación de la API (Swagger) 
├── src/ # Código fuente principal 
│ ├── api/ # Controladores, rutas, middlewares 
│ ├── config/ # Configuración de la app 
│ ├── constants/ # Constantes globales 
│ ├── interfaces/ # Interfaces de TypeScript 
│ ├── models/ # Modelos de datos 
│ ├── responses/ # Respuestas estandarizadas de la API  
│ ├── schemas/ # Esquemas de validación 
│ ├── services/ # Lógica de negocio 
│ ├── tests/ # Pruebas unitarias e integración 
│ ├── utils/ # Funciones utilitarias 
├── package.json # Dependencias y scripts 
├── tsconfig.json # Configuración de TypeScript
````


## Requisitos previos

- Node.js (v16 o superior)
- npm

## Configuración

1. Clona el repositorio:

	```bash
	git clone https://github.com/nuriadevs/fitflow-fullstack
	cd fitflow-app/backend
	```

2.  Instalación de dependencias:

	```bash
	npm install
	```

## Scripts

-   `npm start`: Inicia el servidor en modo desarrollo con nodemon.
    
-   `npm test`: Ejecuta las pruebas con Jest.

## Variables de entorno

Crea un archivo `.env` en la raíz del proyecto y define las siguientes variables:

````
DATABASE_URL=<DATABASE_URL>
JWT_SECRET=<JWT_SECRET>
OPENAI_API_KEY=<YOUR_OPENAI_API_KEY>
MONGODB_URI=<MONGODB_CONNECTION_URI>
PORT=<SERVER_PORT>
CORS_ORIGIN=<ALLOWED_ORIGIN>
NODE_ENV=<ENVIRONMENT>
UPSTASH_VECTOR_REST_URL=<VECTOR_REST_URL>
UPSTASH_VECTOR_REST_TOKEN=<UPSTASH_TOKEN>
````
Puedes personalizar más ajustes en `src/config/env.ts` si es necesario.

## Documentación de la API

La documentación está disponible en `docs/swagger.yaml`.  
Puedes visualizarla con Swagger UI o importarla en herramientas como Postman o Bruno.

## Pruebas

Ejecuta las pruebas con:

`npm test`

## Peticiones al chat

Puedes hacer solicitudes al asistente; ten en cuenta que los datos de los ejercicios están en inglés y el agente también .
- Recommend exercises for biceps.
- Recommend exercises for triceps.
- Recommend a routine for training glutes.

## Demo

<img src="./media/backend-api/backend-api.png" alt="backend api" width="600" />

[Watch video demo backend](https://youtu.be/7JgR5SAsv9U)


## Enlaces útiles
- [OpenAI](https://platform.openai.com/docs/overview)
- [UpStash](https://upstash.com/)
- [MongoDB](https://www.mongodb.com/)

## Resumen

-   No olvides crear tu propio archivo `.env` con las variables necesarias.
    
-   Este proyecto aún está en desarrollo y puede seguir mejorando.