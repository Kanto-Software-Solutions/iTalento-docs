---
sidebar_label: 'Buscar Reseña'
sidebar_position: 1
---

# Buscar Reseña

---

## GET /review

Retorna todas las reseñas públicas en italento.shop.

### URL

**`https://italento.shop/review`**

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/review`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/review")
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
            "idReview": 1,
            "idUser": 2,
            "idGig": 1,
            "createdAt": "2023-10-13T10:10:50.000Z",
            "rating": 4.3,
            "title": "Excelente",
            "description": "Lorem Ipsum sit amet dolo",
        },
        {
            "idReview": 2,
            "idUser": 4,
            "idGig": 2,
            "createdAt": "2023-10-13T10:10:60.000Z",
            "rating": 2.0,
            "title": "Pésimo",
            "description": "Lorem Ipsum sit amet dolo",
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
      <td><code>idReview</code></td>
      <td>int</td>
      <td>Identificador único asignado a la red social.</td>
    </tr>
    <tr>
      <td><code>idUser</code></td>
      <td>string</td>
      <td>ID del usuario que creó la reseña.</td>
    </tr>
    <tr>
      <td><code>idGig</code></td>
      <td>string</td>
      <td>ID de la publicación a la que se refiere la reseña.</td>
    </tr>
    <tr>
      <td><code>createdAt</code></td>
      <td>string</td>
      <td>Fecha de creación de la publicación en formato ISO 8601.</td>
    </tr>
    <tr>
      <td><code>rating</code></td>
      <td>double</td>
      <td>Calificación (del 1 al 5, con 1 decimal).</td>
    </tr>
    <tr>
      <td><code>title</code></td>
      <td>string</td>
      <td>Titulo de la reseña.</td>
    </tr>
    <tr>
      <td><code>description</code></td>
      <td>string</td>
      <td>El contenido de la reseña (máximo 500 caracteres).</td>
    </tr>
  </tbody>
</table>

## GET /review/id

Retorna **unicamente** la información de la reseña a la que pertenece el ID, en caso de no encontrarse devuelve un ERROR 404.

### URL

**`https://italento.shop/review/:id`**

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
      <td>Identificador único asignado a la reseña a solicitar.</td>
    </tr>
  </tbody>
</table>

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/review`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/review")
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
            "idReview": 1,
            "idUser": 2,
            "idGig": 1,
            "createdAt": "2023-10-13T10:10:50.000Z",
            "rating": 4.3,
            "title": "Excelente",
            "description": "Lorem Ipsum sit amet dolo",
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
      <td><code>idReview</code></td>
      <td>int</td>
      <td>Identificador único asignado a la red social.</td>
    </tr>
    <tr>
      <td><code>idUser</code></td>
      <td>string</td>
      <td>ID del usuario que creó la reseña.</td>
    </tr>
    <tr>
      <td><code>idGig</code></td>
      <td>string</td>
      <td>ID de la publicación a la que se refiere la reseña.</td>
    </tr>
    <tr>
      <td><code>createdAt</code></td>
      <td>string</td>
      <td>Fecha de creación de la publicación en formato ISO 8601.</td>
    </tr>
    <tr>
      <td><code>rating</code></td>
      <td>double</td>
      <td>Calificación (del 1 al 5, con 1 decimal).</td>
    </tr>
    <tr>
      <td><code>title</code></td>
      <td>string</td>
      <td>Titulo de la reseña.</td>
    </tr>
    <tr>
      <td><code>description</code></td>
      <td>string</td>
      <td>El contenido de la reseña (máximo 500 caracteres).</td>
    </tr>
  </tbody>
</table>