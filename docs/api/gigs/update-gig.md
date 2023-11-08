---
sidebar_label: 'Actualizar Publicación'
sidebar_position: 3
---

# Actualizar Publicación

---

## PUT /publicaciones/id

Endpoint para actualizar una publicación especifica en italento.shop.

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
      <td>Identificador único asignado a la publicación a editar.</td>
    </tr>
  </tbody>
</table>

### Parámetros de Solicitud (wwwUrlEncoded)

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
      <td>ID del usuario que publicó la oferta. (necesita registro a priori)</td>
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


import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="postman" label="Postman" default>
    <p>PUT:  `https://italento.shop/publicaciones`</p>
    <p>BODY (x-www-form-urlEncoded):</p>
```json   
idGig: 3
name: HelloWorld
description: Un Gig Generico para probar estados
idCategory: 4
idUser: 2
price: 2000000
deliveryDays: 3
```
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch('https://italento.shop/publicacion', {
  method: 'PUT',
  headers: {
    'Content-Type': 'application/x-www-form-urlencoded;charset=UTF-8'
  },
  body: formBody
}
```

:::note[Nota]

Es necesario codificar el cuerpo de la solicitud en forma `form-urlencoded`, para más información ver: [Url Encoded](https://stackoverflow.com/questions/35325370/how-do-i-post-a-x-www-form-urlencoded-request-using-fetch)

:::
  </TabItem>
</Tabs>

### Respuesta

El servidor responde con un código de estado `200 OK` si la publicación se ha actualizado con éxito.
