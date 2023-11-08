---
sidebar_label: 'Borrar Habilidad'
sidebar_position: 4
---

# Borrar Habilidad

---

## DELETE /ability/id

Endpoint para borrar una habilidad especifica en italento.shop.

:::danger[Cuidado!]

Al enviar la solicitud, la habilidad se borrará automáticamente, NO se podrá recuperar.

:::

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
      <td>Identificador único asignado a la habilidad a borrar.</td>
    </tr>
  </tbody>
</table>

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="postman" label="Postman" default>
    DELETE:  `https://italento.shop/ability/1`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
    fetch("https://italento.shop/ability/1", { 
            method: 'DELETE', 
            headers: { 
                'Content-type': 'application/json'
            } 
        });
```
  </TabItem>
</Tabs>


### Respuesta

El servidor responde con un código de estado `200 OK` si la reseña se ha eliminado con éxito.

