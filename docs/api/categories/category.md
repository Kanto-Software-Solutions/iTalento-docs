---
sidebar_label: 'Buscar Categoría'
sidebar_position: 1
---

# Buscar Categorías

---

## Introducción

La cátegoria es uno de los recursos principales de iTalento. Una categoría es la forma en que tanto publicaciones como creadores se dividen, es por esto que las cátegorias son estaticas, nunca se crearán ni borrarán categorías sin un aviso con suficiente anticipación.

Al punto final de categorías solo se pueden realizar solicitudes HTTP GET, y estas pueden usar un ID.

## GET /categorias

Retorna información acerca de todas las categorías existentes en iTalento.

### URL

**`https://italento.shop/categorias`**

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/categorias`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/categorias")
  .then((response) => response.json())
  .then((json) => console.log(json));
```
  </TabItem>
</Tabs>

### Ejemplo de Respuesta

```json
{
    "results": [
        {
            "idCategory": 1,
            "name": "Diseño de Logos",
            "imgUrl": null,
            "descripcion": null
        },
        {
            "idCategory": 2,
            "name": "Ilustraciones",
            "imgUrl": null,
            "descripcion": null
        }
        ...
    ]
}
```

### Parámetros de Respuesta

<table>
  <thead>
    <tr>
      <th width="20%">Nombre</th>
      <th width="20%">Tipo</th>
      <th width="40%">Descripción</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>idCategory</code></td>
      <td>int</td>
      <td>Identificador único asignado a la categoría.</td>
    </tr>
    <tr>
      <td><code>name</code></td>
      <td>string</td>
      <td>El nombre de la cátegoria, se trata de ser lo más conciso posible mientras se intenta abarcar bastantes temas.</td>
    </tr>
    <tr>
      <td><code>imgUrl</code></td>
      <td>string</td>
      <td>Una URL que dirije a un espacio en Cloudinary, el servicio de hosting de imágenes el cual provee a iTalento.</td>
    </tr>
    <tr>
      <td><code>descripcion</code></td>
      <td>string</td>
      <td>Descripción de lo que es cada categoría. Se tiene un limite de 80 caracteres, se debe ser breve.</td>
    </tr>
  </tbody>
</table>

## GET /categorias/id

Retorna **unicamente** la información de la categoría a la que pertenece el ID, en caso de no encontrarse devuelve un ERROR 404.

### URL

**`https://italento.shop/categorias/:id`**

### Parámetros de la ruta

<table>
  <thead>
    <tr>
      <th width="20%">Nombre</th>
      <th width="20%">Tipo</th>
      <th width="40%">Descripción</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>id</code></td>
      <td>int</td>
      <td>Identificador único asignado a la categoría a solicitar.</td>
    </tr>
  </tbody>
</table>

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/categorias/1`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/categorias/1")
  .then((response) => response.json())
  .then((json) => console.log(json));
```
  </TabItem>
</Tabs>

### Ejemplo de Respuesta

```json
{
    "results": [
        {
            "idCategory": 1,
            "name": "Diseño de Logos",
            "imgUrl": null,
            "descripcion": null
        }
    ]
}
```

### Parámetros de Respuesta

<table>
  <thead>
    <tr>
      <th width="20%">Nombre</th>
      <th width="20%">Tipo</th>
      <th width="40%">Descripción</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>idCategory</code></td>
      <td>int</td>
      <td>Identificador único asignado a la categoría.</td>
    </tr>
    <tr>
      <td><code>name</code></td>
      <td>string</td>
      <td>El nombre de la cátegoria, se trata de ser lo más conciso posible mientras se intenta abarcar bastantes temas.</td>
    </tr>
    <tr>
      <td><code>imgUrl</code></td>
      <td>string</td>
      <td>Una URL que dirije a un espacio en Cloudinary, el servicio de hosting de imágenes el cual provee a iTalento.</td>
    </tr>
    <tr>
      <td><code>descripcion</code></td>
      <td>string</td>
      <td>Descripción de lo que es cada categoría. Se tiene un limite de 80 caracteres, se debe ser breve.</td>
    </tr>
  </tbody>
</table>

