---
sidebar_label: 'Borrar Reseña'
sidebar_position: 2
---

# Borrar Reseña

---

## DELETE /review/id

Endpoint para borrar una reseña especifica en italento.shop.

:::danger[Cuidado!]

Al enviar la solicitud, la reseña se borrará automáticamente, NO se podrá recuperar.

:::

:::info

La función de borrar solo está disponible si eres el propietario de la reseña.

:::

### URL

- `italento.shop/review/:id`

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
      <td>Identificador único asignado a la reseña a borrar.</td>
    </tr>
  </tbody>
</table>

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="postman" label="Postman" default>
    DELETE:  `https://italento.shop/review/1`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
    fetch("https://italento.shop/review/1", { 
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

