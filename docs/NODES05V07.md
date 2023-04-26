# VIDEO 07 - Ejercicio: API Rest con launch.json, async, objetos y desplegada en Vercel

En este vídeo debes aplicar varios cambios sobre la API de libros en las sesiones anteriores.

Si no tienes el ejercicio resuelto puedes utilizar nuestra solución como punto de partida:

<https://github.com/The-Valley-School/node-s4-solution-complete-crud>

Los cambios a realizar serían:

- Cambiar todas las promesas por async/await
- Añadir el fichero launch.json y depurar tu código para aprender a usar el modo debug de VSCode
- Añade el objeto publisher (editorial) dentro de los libros
- Corrige el fichero index.js para que sea asíncrono y espere a la conexión para seguir ejecutando el código con await connect();
- Modifica tu código para que el nombre de la base de datos lo lea de una variable de entorno, en local usa la de desarrollo (DEVELOPMENT)
- Añade el fichero vercel.json y despliega tu proyecto en Vercel haciendo que use la base de datos de PRODUCTION

Recuerda que puedes encontrar todo el código que hemos visto durante la sesión en este repositorio de Git:

<https://github.com/The-Valley-School/node-s5-debug-deploy>
