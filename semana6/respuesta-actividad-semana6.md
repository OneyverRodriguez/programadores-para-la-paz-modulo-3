# Respuesta a la Actividad - Semana 6, Módulo 3

## Lo Solicitado

Se solicitó crear un servidor web utilizando **Express.js** que cumpliera con los siguientes requisitos:

- Configurar un servidor Node.js con el framework Express
- Crear una ruta HTTP POST en el endpoint `/registro`
- Recibir datos JSON con los campos `nombre` y `mensaje`
- Procesar los datos recibidos
- Devolver una respuesta JSON que confirme la recepción de los datos
- El servidor debe ejecutarse en el puerto 3000

## Solución Implementada

Se creó un servidor Express (`server.js`) con la siguiente estructura:

### 1. Inicialización y Configuración
```javascript
const express = require('express');
const app = express();
app.use(express.json());
```
Se importó Express, se creó la aplicación y se configuró el middleware para procesar JSON.

### 2. Ruta POST `/registro`
```javascript
app.post('/registro', (req, res) => {
    const nombre = req.body.nombre;
    const mensaje = req.body.mensaje;
    
    res.json({
        estado: "Datos recibidos",
        nombre: nombre,
        mensaje: mensaje
    });
});
```
La ruta extrae los datos del cuerpo de la solicitud y los devuelve en la respuesta.

### 3. Inicio del Servidor
```javascript
app.listen(3000, () => {
    console.log('Servidor ejecutándose en puerto 3000');
});
```
El servidor inicia en el puerto 3000 y muestra un mensaje de confirmación.

## Lo Recibido

La solución fue probada exitosamente en Postman, enviando una solicitud POST a `http://localhost:3000/registro` con los siguientes datos:

**Datos Enviados (Request Body):**
```json
{
    "nombre": "Oneyver Rodriguez",
    "mensaje": "Hola comunidad, Este es un mensaje de prueba, enviado por Oneyver Rodriguez Novo del Programa Programadores para la paz, probando el Servidor para la actividad de la Semana 6 - Modulo 3"
}
```

**Respuesta Recibida:**
```json
{
    "estado": "Datos recibidos",
    "nombre": "Oneyver Rodriguez",
    "mensaje": "Hola comunidad, Este es un mensaje de prueba, enviado por Oneyver Rodriguez Novo del Programa Programadores para la paz, probando el Servidor para la actividad de la Semana 6 - Modulo 3"
}
```

## Conclusión

✅ **La actividad fue completada con éxito.** El servidor Express funciona correctamente, recibe datos JSON en la ruta especificada, procesa la información y devuelve la respuesta esperada. La prueba en Postman confirma que todos los requerimientos fueron cumplidos satisfactoriamente.

---

**Desarrollador:** Oneyver Rodriguez Novo  
**Programa:** Programadores para la Paz  
**Módulo:** 3  
**Semana:** 6  
**Fecha:** 6 de junio de 2026

