# VIDEO 01 - Inspeccionar y depurar código en Node

En este vídeo hemos visto cómo podemos depurar nuestro código Node dentro de visual studio code:

<https://code.visualstudio.com/docs/nodejs/nodejs-debugging>

Para ello hemos creado un fichero launch.json dentro de la carpeta .vscode que tiene este contenido:

```jsx
{
  // Use IntelliSense para saber los atributos posibles.
  // Mantenga el puntero para ver las descripciones de los existentes atributos.
  // Para más información, visite: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Iniciar el programa",
      "skipFiles": ["<node_internals>/**"],
      "program": "${workspaceFolder}/index.js"
    }
  ]
}
```

Gracias a eso podemos usar la consola de Visual Studio para ir moviéndonos por el código y analizando el valor de las variables y los flujos que sigue nuestro código.

![Untitled](/docs/assets/Untitled.png)
