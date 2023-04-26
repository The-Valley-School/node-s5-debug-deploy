# VIDEO 04 - Despliegue en Vercel

En este vídeo hemos visto cómo podemos desplegar nuestro backend en Vercel para que esté disponible para ser usado desde cualquier sitio:

<https://vercel.com/>

Después de registrarnos e importar el proyecto, el paso más importante es crear un fichero vercel.json para que podamos indicar a vercel qué fichero debe ejecutar:

```jsx
{
  "builds": [
    {
      "src": "index.js",
      "use": "@vercel/node"
    }
  ],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "index.js"
    }
  ]
}
```
