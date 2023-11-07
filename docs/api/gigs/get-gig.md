---
sidebar_label: 'Buscar Publicación'
sidebar_position: 1
---


# Publicación

---

## GET /publicaciones

Endpoint para obtener las publicaciones disponibles en italento.shop.

### URL

- `italento.shop/publicaciones`

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/publicaciones`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/publicaciones")
  .then((response) => response.json())
  .then((json) => console.log(json));
```
  </TabItem>
</Tabs>

### Ejemplo de respuesta

```json
{
    "results": [
        {
            "idGig": 1,
            "name": "Logos minimalistas",
            "description": "Hago logos a domicilio",
            "createdAt": "2023-10-13T10:10:50.000Z",
            "idCategory": 1,
            "idUser": 1,
            "price": 10,
            "deliveryDays": 7
        }
    ]
}
```

### Parámetros de respuesta

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
      <td><code>idGig</code></td>
      <td>int</td>
      <td>ID único de la publicación.</td>
    </tr>
    <tr>
      <td><code>name</code></td>
      <td>string</td>
      <td>Nombre de la publicación.</td>
    </tr>
    <tr>
      <td><code>description</code></td>
      <td>int</td>
      <td>Descripción de la publicación.</td>
    </tr>
    <tr>
      <td><code>createdAt</code></td>
      <td>string</td>
      <td>Fecha de creación de la publicación en formato ISO 8601.</td>
    </tr>
    <tr>
      <td><code>idCategory</code></td>
      <td>int</td>
      <td>Identificador de la publicación en la que está la imagen.</td>
    </tr>
    <tr>
      <td><code>idUser</code></td>
      <td>int</td>
      <td>ID del usuario que publicó la oferta.</td>
    </tr>
    <tr>
      <td><code>price</code></td>
      <td>int</td>
      <td>Precio de la publicación en dólares.</td>
    </tr>
    <tr>
      <td><code>deliveryDays</code></td>
      <td>int</td>
      <td>Días de entrega estimados.</td>
    </tr>
  </tbody>
</table>

:::note[Nota]

Las imágenes asociadas a cada publicación se almacenan en su propio espacio, con una relación por medio del `idGig`, para más información ver: [Imagen](../images/introduction.md)

:::

## GET /publicaciones/id

Endpoint para obtener información detallada de una publicación específica en italento.shop.

### URL

- `italento.shop/publicaciones/:id`

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
      <td>Identificador único asignado a la publicación.</td>
    </tr>
  </tbody>
</table>

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/publicaciones/1`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/publicaciones/1")
  .then((response) => response.json())
  .then((json) => console.log(json));
```
  </TabItem>
</Tabs>

### Ejemplo de respuesta

```json
{
    "results": [
        {
            "idGig": 1,
            "name": "Logos minimalistas",
            "description": "Hago logos a domicilio",
            "createdAt": "2023-10-13T10:10:50.000Z",
            "idCategory": 1,
            "idUser": 1,
            "price": 10,
            "deliveryDays": 7
        }
    ]
}
```

### Parámetros de respuesta

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
      <td><code>idGig</code></td>
      <td>int</td>
      <td>ID único de la publicación.</td>
    </tr>
    <tr>
      <td><code>name</code></td>
      <td>string</td>
      <td>Nombre de la publicación.</td>
    </tr>
    <tr>
      <td><code>description</code></td>
      <td>int</td>
      <td>Descripción de la publicación.</td>
    </tr>
    <tr>
      <td><code>createdAt</code></td>
      <td>string</td>
      <td>Fecha de creación de la publicación en formato ISO 8601.</td>
    </tr>
    <tr>
      <td><code>idCategory</code></td>
      <td>int</td>
      <td>Identificador de la publicación en la que está la imagen.</td>
    </tr>
    <tr>
      <td><code>idUser</code></td>
      <td>int</td>
      <td>ID del usuario que publicó la oferta.</td>
    </tr>
    <tr>
      <td><code>price</code></td>
      <td>int</td>
      <td>Precio de la publicación en dólares.</td>
    </tr>
    <tr>
      <td><code>deliveryDays</code></td>
      <td>int</td>
      <td>Días de entrega estimados.</td>
    </tr>
  </tbody>
</table>

## GET /publicaciones/user/id

Endpoint para obtener todas las publicaciones de un usuario específico en italento.shop.

### URL

- `italento.shop/publicaciones/user/:id`

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
      <td>Identificador único asignado al usuario propietario de las publicaciones.</td>
    </tr>
  </tbody>
</table>

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/publicaciones/user/1`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/publicaciones/user/1")
  .then((response) => response.json())
  .then((json) => console.log(json));
```
  </TabItem>
</Tabs>

### Ejemplo de respuesta

```json
{
    "results": [
        {
            "idGig": 1,
            "name": "Logos minimalistas",
            "description": "Hago logos a domicilio",
            "createdAt": "2023-10-13T10:10:50.000Z",
            "idCategory": 1,
            "idUser": 1,
            "price": 10,
            "deliveryDays": 7
        }
    ]
}
```

### Parámetros de respuesta

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
      <td><code>idGig</code></td>
      <td>int</td>
      <td>ID único de la publicación.</td>
    </tr>
    <tr>
      <td><code>name</code></td>
      <td>string</td>
      <td>Nombre de la publicación.</td>
    </tr>
    <tr>
      <td><code>description</code></td>
      <td>int</td>
      <td>Descripción de la publicación.</td>
    </tr>
    <tr>
      <td><code>createdAt</code></td>
      <td>string</td>
      <td>Fecha de creación de la publicación en formato ISO 8601.</td>
    </tr>
    <tr>
      <td><code>idCategory</code></td>
      <td>int</td>
      <td>Identificador de la publicación en la que está la imagen.</td>
    </tr>
    <tr>
      <td><code>idUser</code></td>
      <td>int</td>
      <td>ID del usuario que publicó la oferta.</td>
    </tr>
    <tr>
      <td><code>price</code></td>
      <td>int</td>
      <td>Precio de la publicación en dólares.</td>
    </tr>
    <tr>
      <td><code>deliveryDays</code></td>
      <td>int</td>
      <td>Días de entrega estimados.</td>
    </tr>
  </tbody>
</table>
