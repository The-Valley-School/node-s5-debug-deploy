# VIDEO 06 - BBDD para DEV y PROD

En este vídeo hemos visto cómo podemos mantener dos bases de datos dentro del plan de Vercel, de manera que usemos dos bases de datos:

- Development para desarrollo
- Production para desplegar en Vercel

De esa manera podemos desarrollar y trastear sin miedo de romper la API de producción o de perder datos.

Para ello hemos creado las dos bases de datos en mongodb:

![Untitled](/docs/assets/Untitled%201.png)

Después hemos configurado en nuestro fichero .env que queremos usar DEVELOPMENT:

```jsx
DB_URL = "mongodb+srv://franlindebl:CV9z0......";
DB_NAME = "DEVELOPMENT";
```

En Vercel hemos añadido la variable de entorno para indicar que queremos usar PRODUCTION:

![Untitled](/docs/assets/Untitled%202.png)

Y hemos leído esa variable desde nuestro fichero db.js:

```jsx
// Cargamos variables de entorno
require("dotenv").config();
const DB_CONNECTION = process.env.DB_URL;
const DB_NAME = process.env.DB_NAME;

// Importamos librerías
const mongoose = require("mongoose");

// Configuración de la conexión a Mongo
const config = {
  useNewUrlParser: true,
  useUnifiedTopology: true,
  serverSelectionTimeoutMS: 5000,
  dbName: DB_NAME,
};

const connect = async () => {
  const database = await mongoose.connect(DB_CONNECTION, config);
  const name = database.connection.name;
  const host = database.connection.host;
  console.log(`Conectado a la base de datos ${name} en el host ${host}`);
  return database;
};

module.exports = { connect };
```

Recuerda que puedes encontrar todo el código que hemos visto durante la sesión en este repositorio de Git:

<https://github.com/The-Valley-School/node-s5-debug-deploy>
