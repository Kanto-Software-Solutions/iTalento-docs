---
sidebar_label: 'Crear Habilidad'
sidebar_position: 2
---

# Crear Habilidad

---

## POST /ability

Endpoint para crear una nueva habilidad en italento.shop.

### URL

- `italento.shop/publicaciones`

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
    <p>POST:  `https://italento.shop/ability`</p>
    <p>BODY (x-www-form-urlEncoded):</p>
```json   
idABility: 10
name: Programación en PHP
```
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch('https://italento.shop/ability', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/x-www-form-urlencoded;charset=UTF-8'
  },
  body: formBody
})
```

:::note[Nota]

Es necesario codificar el cuerpo de la solicitud en forma `form-urlencoded`, para más información ver: [Url Encoded](https://stackoverflow.com/questions/35325370/how-do-i-post-a-x-www-form-urlencoded-request-using-fetch)

:::
  </TabItem>
</Tabs>

### Respuesta

El servidor responde con un código de estado `200 OK` si la habilidad se ha creado con éxito.