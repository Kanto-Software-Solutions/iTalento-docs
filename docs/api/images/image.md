---
sidebar_label: 'Buscar Imagen'
sidebar_position: 2
---

# Buscar Imagen

---

## GET /imagenes

Retorna todas las imagenes de las publicaciones en iTalento, entiéndase como publicación, la oferta de un freelancer.

### URL

**`https://italento.shop/imagenes`**

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/imagenes`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/imagenes")
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
            "idImage": 1,
            "url": null,
            "idUser": 7,
            "idGig": 6
        },
        {
            "idImage": 2,
            "url": null,
            "idUser": 8,
            "idGig": 1
        },
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
      <td><code>idImage</code></td>
      <td>int</td>
      <td>Identificador único asignado a la imagen, el ID es diferente a el asignado por Cloudinary.</td>
    </tr>
    <tr>
      <td><code>url</code></td>
      <td>string</td>
      <td>Una URL que dirije a un la imagen respectiva alojada en Cloudinary.</td>
    </tr>
    <tr>
      <td><code>idUser</code></td>
      <td>int</td>
      <td>Identificador del usuario que subió la imagen.</td>
    </tr>
    <tr>
      <td><code>idGig</code></td>
      <td>int</td>
      <td>Identificador de la publicación en la que está la imagen.</td>
    </tr>
  </tbody>
</table>

## GET /imagenes/id

Retorna **únicamente** la información de la imagen a la que pertenece el ID, en caso de no encontrarse devuelve un ERROR 404.

### URL

**`https://italento.shop/imagenes/:id`**

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
      <td>Identificador único asignado a la imagen a solicitar.</td>
    </tr>
  </tbody>
</table>

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/imagenes/1`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/imagenes/1")
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
            "idImage": 1,
            "url": null,
            "idUser": 7,
            "idGig": 6
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
      <td><code>idImage</code></td>
      <td>int</td>
      <td>Identificador único asignado a la imagen, el ID es diferente a el asignado por Cloudinary.</td>
    </tr>
    <tr>
      <td><code>url</code></td>
      <td>string</td>
      <td>Una URL que dirije a un la imagen respectiva alojada en Cloudinary.</td>
    </tr>
    <tr>
      <td><code>idUser</code></td>
      <td>int</td>
      <td>Identificador del usuario que subió la imagen.</td>
    </tr>
    <tr>
      <td><code>idGig</code></td>
      <td>int</td>
      <td>Identificador de la publicación en la que está la imagen.</td>
    </tr>
  </tbody>
</table>


