---
sidebar_label: 'Editar Habilidad'
sidebar_position: 3
---

# Editar Habilidad

---

## PUT /publicaciones/id

Endpoint para editar (actualizar) una habilidad especifica en italento.shop.

### URL

- `italento.shop/ability/:id`

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
      <td>Identificador único asignado a la habilidad a editar.</td>
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
      <td><code>idAbility</code></td>
      <td>int</td>
      <td>ID único de la habilidad.</td>
    </tr>
    <tr>
      <td><code>name</code></td>
      <td>string</td>
      <td>Nombre de la habilidad.</td>
    </tr>
  </tbody>
</table>


import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="postman" label="Postman" default>
    <p>PUT:  `https://italento.shop/ability/10`</p>
    <p>BODY (x-www-form-urlEncoded):</p>
```json   
idGig: 10
name: Programación en PHP con PHPStorm
```
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch('https://italento.shop/ability/10', {
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

El servidor responde con un código de estado `200 OK` si la habilidad se ha actualizado con éxito.
