---
sidebar_label: 'Buscar Red Social'
sidebar_position: 1
---


# Buscar Categorías

---

## GET /redsocial

Retorna información acerca de todas las redes sociales disponibles para integración con iTalento.

### URL

**`https://italento.shop/redsocial`**

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/redsocial`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/redsocial")
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
            "idSNetwork": 1,
            "name": "GitHub",
            "link": "https://github.com/",
            "imgUrl": null,
            "idUser": 1
        },
        {
            "idSNetwork": 2,
            "name": "LinkedIn",
            "link": "https://www.linkedin.com/feed/",
            "imgUrl": null,
            "idUser": 2
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
      <td><code>idSNetwork</code></td>
      <td>int</td>
      <td>Identificador único asignado a la red social.</td>
    </tr>
    <tr>
      <td><code>name</code></td>
      <td>string</td>
      <td>El nombre de la red social.</td>
    </tr>
    <tr>
      <td><code>link</code></td>
      <td>string</td>
      <td>Una URL que dirije a el perfil personal del usuario en esa red social.</td>
    </tr>
    <tr>
      <td><code>imgUrl</code></td>
      <td>string</td>
      <td>Url de la imagen, proveida por Cloudinary.</td>
    </tr>
    <tr>
      <td><code>idUser</code></td>
      <td>string</td>
      <td>Id del usuario al que pertenece el link de la red social.</td>
    </tr>
  </tbody>
</table>

## GET /redes/id

Retorna **unicamente** la información de la red a la que pertenece el ID, en caso de no encontrarse devuelve un ERROR 404.

### URL

**`https://italento.shop/redes/:id`**

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
    GET:  `https://italento.shop/redsocial`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/redsocial")
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
            "idSNetwork": 1,
            "name": "GitHub",
            "link": "https://github.com/",
            "imgUrl": null,
            "idUser": 1
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
      <td><code>idSNetwork</code></td>
      <td>int</td>
      <td>Identificador único asignado a la red social.</td>
    </tr>
    <tr>
      <td><code>name</code></td>
      <td>string</td>
      <td>El nombre de la red social.</td>
    </tr>
    <tr>
      <td><code>link</code></td>
      <td>string</td>
      <td>Una URL que dirije a el perfil personal del usuario en esa red social.</td>
    </tr>
    <tr>
      <td><code>imgUrl</code></td>
      <td>string</td>
      <td>Url de la imagen, proveida por Cloudinary.</td>
    </tr>
    <tr>
      <td><code>idUser</code></td>
      <td>string</td>
      <td>Id del usuario al que pertenece el link de la red social.</td>
    </tr>
  </tbody>
</table>