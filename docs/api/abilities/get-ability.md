---
sidebar_label: 'Buscar Habilidad'
sidebar_position: 1
---

# Buscar Habilidad

---

## GET /abilities

Retorna información acerca de las habilidades disponibles en iTalento.

### URL

**`https://italento.shop/ability`**

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/ability`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/ability")
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
            "idAbility": 1,
            "name": "Programación en Python",
        },
        {
            "idAbility": 2,
            "name": "Diseño Gráfico",
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
      <td><code>idAbility</code></td>
      <td>int</td>
      <td>Identificador único asignado a la habilidad.</td>
    </tr>
    <tr>
      <td><code>names</code></td>
      <td>string</td>
      <td>Nombre de la habilidad.</td>
    </tr>
  </tbody>
</table>


## GET /abilities/id

Retorna información acerca de una habilidad especificado por su Id.

### URL

**`https://italento.shop/ability/:id`**

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
      <td>Identificador único asignado a la habilidad a solicitar.</td>
    </tr>
  </tbody>
</table>

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/ability/1`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/ability/1")
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
            "idAbility": 1,
            "name": "Programación en Python",
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
      <td><code>idAbility</code></td>
      <td>int</td>
      <td>Identificador único asignado a la habilidad.</td>
    </tr>
    <tr>
      <td><code>names</code></td>
      <td>string</td>
      <td>Nombre de la habilidad.</td>
    </tr>
  </tbody>
</table>


