# VIDEO 03 - Objetos anidados y validaciones

En este vídeo hemos visto que podemos almacenar objetos dentro de propiedades. Para demostrarlo hemos añadido un objeto address dentro de User:

```jsx
const mongoose = require("mongoose");
const Schema = mongoose.Schema;

// Creamos el schema del usuario
const userSchema = new Schema(
  {
    firstName: {
      type: String,
      required: true,
    },
    lastName: {
      type: String,
      required: true,
    },
    phone: {
      type: String,
      required: false,
    },
    address: {
      type: {
        street: {
          type: String,
          required: true,
        },
        number: {
          type: Number,
          required: true,
        },
        city: {
          type: String,
          required: true,
        },
      },
      required: false,
    },
  },
  {
    timestamps: true,
  }
);

const User = mongoose.model("User", userSchema);
module.exports = { User };
```
