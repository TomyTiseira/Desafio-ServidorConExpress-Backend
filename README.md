# Servidor con express

Realizar un proyecto de servidor basado en node.js que utilice el módulo express e implemente los siguientes endpoints en el puerto 8080:

- Ruta get '/productos' que devuelva un array con todos los productos disponibles en el servidor.
- Ruta get '/productoRandom' que devuelva un producto elegido al azar entre todos los productos disponibles.

Incluir un archivo 'productos.json' y utilizar la clase Contenedor del desafío anterior para acceder a los datos persistidos del servidor.

Antes de iniciar el servidor, colocar en el archivo 'productos.json' tres productos como en el ejemplo del desafío anterior.
Con el formato:

```json
[
  {
    "title": "Escuadra",
    "price": 123.45,
    "thumbnail": "https://cdn3.iconfinder.com/data/icons/education-209/64/ruler-triangle-stationary-school-256.png",
    "id": 1
  },
  {
    "title": "Calculadora",
    "price": 234.56,
    "thumbnail": "https://cdn3.iconfinder.com/data/icons/education-209/64/calculator-math-tool-school-256.png",
    "id": 2
  },
  {
    "title": "Globo Terráqueo",
    "price": 345.67,
    "thumbnail": "https://cdn3.iconfinder.com/data/icons/education-209/64/globe-earth-geograhy-planet-school-256.png",
    "id": 3
  }
]
```

## Métodos clase Contenedor

- save(Object): Number - Recibe un objeto, lo guarda en el archivo, devuelve el id asignado.
- getById(Number): Object - Recibe un id y devuelve el objeto con ese id, o null si no está.
- getAll(): Object[] - Devuelve un array con los objetos presentes en el archivo.
- deleteById(Number): void - Elimina del archivo el objeto con el id buscado.
- deleteAll(): void - Elimina todos los objetos presentes en el archivo.

### Métodos auxiliares

- getProducts(): void - Guarda los productos obtenidos del archivo 'productos.json' en el atributo 'products' de la clase Contenedor.
- updateId(Object[]): void - Actualiza los id del array de productos.
- idRandom() : Number - Método encargado de buscar los datos necesarios para la obtención del id random, generarlo y retornarlo.
