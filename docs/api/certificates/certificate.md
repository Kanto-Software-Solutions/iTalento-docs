---
sidebar_label: 'Buscar Certificado'
sidebar_position: 1
---

# Buscar Certificado

---

## Introducción

Los certificados son una forma para los usuarios de iTalento de darse a ver a sus clientes, iTalento admite cualquier certificado que haya sido expedido por una institución educativa, tales como colegios, universidades, institutos y entidades privadas.

Al punto final de certificados solo se pueden realizar solicitudes HTTP GET, y estas pueden usar un ID.

## GET /certificados

Retorna información acerca de todas las certificados existentes en iTalento.

### URL

**`https://italento.shop/certificado`**

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/certificado`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/certificado")
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
            "idCertificate": 1,
            "name": "Administrador de Empresas",
            "institution": "Universidad Nacional de Colombia",
            "year": 2020
        },
        {
            "idCertificate": 2,
            "name": "Ingeniero de Sistemas",
            "institution": "Universidad de los Andes",
            "year": 2023
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
      <td><code>idCertificate</code></td>
      <td>int</td>
      <td>Identificador único asignado al certificado (para propósitos dentro de la base de datos).</td>
    </tr>
    <tr>
      <td><code>name</code></td>
      <td>string</td>
      <td>El nombre del titulo del certificado, puede ser un curso, diplomado, etc.</td>
    </tr>
    <tr>
      <td><code>institution</code></td>
      <td>string</td>
      <td>El nombre de la entidad que expide el certificado.</td>
    </tr>
    <tr>
      <td><code>year</code></td>
      <td>int</td>
      <td>El año de expedición del certificado.</td>
    </tr>
  </tbody>
</table>

## GET /categorias/id

Retorna **unicamente** la información del certificado al que pertenece el ID, en caso de no encontrarse devuelve un ERROR 404.

### URL

**`https://italento.shop/certificados/:id`**

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
      <td>Identificador único asignado al certificado solicitado.</td>
    </tr>
  </tbody>
</table>

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/certificado/1`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/certificado/1")
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
            "idCertificate": 1,
            "name": "Administrador de Empresas",
            "institution": "Universidad Nacional de Colombia",
            "year": 2020
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
      <td><code>idCertificate</code></td>
      <td>int</td>
      <td>Identificador único asignado al certificado (para propósitos dentro de la base de datos).</td>
    </tr>
    <tr>
      <td><code>name</code></td>
      <td>string</td>
      <td>El nombre del titulo del certificado, puede ser un curso, diplomado, etc.</td>
    </tr>
    <tr>
      <td><code>institution</code></td>
      <td>string</td>
      <td>El nombre de la entidad que expide el certificado.</td>
    </tr>
    <tr>
      <td><code>year</code></td>
      <td>int</td>
      <td>El año de expedición del certificado.</td>
    </tr>
  </tbody>
</table>

