---
sidebar_label: 'Buscar Usuario'
sidebar_position: 1
---

# Buscar Categorías

---

## Introducción

En iTalento, el usuario contiene la mayoria de la información necesaria para el funcionamiento correcto de la aplicación, la mayoría de objetos hacen referencia a este e iteran sobre el. Los usuarios se crean gracias al login de auth0 que almacena y procesa la información confidencial e importante como contraseñas. iTalento NO almacena contraseñas, esto nos permite estar a salvo de filtraciones.

Por consiguiente a usuarios solo se pueden realizar solicitudes HTTP GET para su propio usuario, para más información visita [Login](/inicio-rapido/login).

## GET /usuario/:id

Retorna información acerca de el usuario al que le pertenece el ID.

### URL

**`https://italento.shop/usuario/:id`**

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
      <td>Identificador único del usuario solicitado.</td>
    </tr>
  </tbody>
</table>

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

<Tabs>
  <TabItem value="postman" label="Postman" default>
    GET:  `https://italento.shop/usuario/1`
  </TabItem>
  <TabItem value="code" label="JS">
    ```js
fetch("https://italento.shop/usuario/1")
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
            "idUser": 1,
            "names": "JOHN",
            "lastNames": "DOE",
            "email": "test@mail.com",
            "isVerified": 0,
            "nickname": "jdoe",
            "profileImage": "yo.png",
            "isFreelancer": 0,
            "birthDate": "2000-05-08T05:00:00.000Z",
            "country": "Colombia",
            "acceptedTerms": 0,
            "personalId": "1192793509"
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
      <td><code>idUser</code></td>
      <td>int</td>
      <td>Identificador único asignado al usuario.</td>
    </tr>
    <tr>
      <td><code>names</code></td>
      <td>string</td>
      <td>Nombre/s del usuario.</td>
    </tr>
    <tr>
      <td><code>lastNames</code></td>
      <td>string</td>
      <td>Apellidos del usuario.</td>
    </tr>
    <tr>
      <td><code>email</code></td>
      <td>string</td>
      <td>Correo eléctronico del usuario.</td>
    </tr>
    <tr>
      <td><code>isVerified</code></td>
      <td>int</td>
      <td>Número (0 o 1) que representa si el usuario tiene su correo verificado.</td>
    </tr>
    <tr>
      <td><code>nickname</code></td>
      <td>string</td>
      <td>El alias del usuario.</td>
    </tr>
    <tr>
      <td><code>profileImage</code></td>
      <td>string</td>
      <td>El link a la foto de perfil, subida en Cloudinary o proveida por Google</td>
    </tr>
    <tr>
      <td><code>isFreelancer</code></td>
      <td>int</td>
      <td>Número (0 o 1) que representa si el usuario es un freelancer.</td>
    </tr>
    <tr>
      <td><code>birthDate</code></td>
      <td>string</td>
      <td>Fecha de nacimiento en formato ISO.</td>
    </tr>
    <tr>
      <td><code>country</code></td>
      <td>string</td>
      <td>El país de residencia.</td>
    </tr>
    <tr>
      <td><code>acceptedTerms</code></td>
      <td>int</td>
      <td>Número (0 o 1) que representa si el usuario ya aceptó los términos y condiciones del servicio.</td>
    </tr>
    <tr>
      <td><code>personalId</code></td>
      <td>string</td>
      <td>Número de Indentificación personal, puede ser cédulo, DNI, etc.</td>
    </tr>
  </tbody>
</table>

## Recursos Adicionales

- [Login y Registro](/inicio-rapido/login)
- [Auth0](https://auth0.com/docs)