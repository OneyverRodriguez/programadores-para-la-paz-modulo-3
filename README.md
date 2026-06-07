# Programadores para la Paz - Módulo 3

Repositorio creado para el desarrollo de las actividades del Módulo 3 del programa **Programadores para la Paz**.

## Estructura del repositorio

- `semana6/`: actividad de servidor Express con rutas `POST` para recibir datos JSON.
- `semana7/`: actividad de servidor Express para registrar y consultar reportes con rutas `GET` y `POST`.

## Semana 6

En la carpeta `semana6` se encuentra un servidor básico con Express que procesa solicitudes `POST`:

- `POST /registro`: recibe `nombre` y `mensaje` en formato JSON.
- `POST /incidencia`: recibe `tipo` y `descripcion` en formato JSON.

Archivo principal: `semana6/server.js`.

Ejemplo de ejecución:

```powershell
cd C:\programadores-para-la-paz-modulo-3\semana6
npm install
node server.js
```

## Semana 7

En la carpeta `semana7` se encuentra un servidor Express que maneja un arreglo en memoria para almacenar reportes.

- `GET /reportes`: devuelve la lista completa de reportes registrados.
- `POST /reportes`: crea un nuevo reporte con `tipo` y `descripcion`.

Archivo principal: `semana7/server.js`.

Ejemplo de ejecución:

```powershell
cd C:\programadores-para-la-paz-modulo-3\semana7
npm install
node server.js
```

## Archivos de apoyo

- `semana6/respuesta-actividad-semana6.md`: respuesta escrita de la actividad de la semana 6.
- `semana7/ejemplos-reportes.txt`: ejemplo de respuesta para la actividad de la semana 7.
- `semana7/preguntas-semana7.txt`: respuestas de la guía de preguntas de la semana 7.

## Nota

Los servidores usan el puerto `3000`, por lo que solo puede ejecutarse uno a la vez si ambos quedan activos en la misma máquina.
