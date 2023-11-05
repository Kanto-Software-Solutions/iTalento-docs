---
sidebar_label: 'Creando tu primera solicitud'
sidebar_position: 2
---

# Comenzando
---
## Haciendo tu primera solicitud a la API de iTalento

Esta guía te guiará por algunos pasos que podrías seguir para hacer tu primera solicitud. Este es un gran recurso para ayudarte una vez que te hayas registrado a una cuenta de iTalento. 

En esta guía vamos a utilizar [Postman](https://www.postman.com/product/what-is-postman/), por lo que un conocimiento básico de este es necesario para el seguimiento de esta guía.

### Paso 1. Identificar el "punto final" de la API a usar

La API de iTalento permite realizar una cantidad de acciones distintas usando código que es ejecutado automáticamente al realizar una búsqueda dentro de la página de iTalento.

Tenemos una lista completa de los puntos finales que están disponibles vía API listados en nuestro [Índice de Referencia], por el momento usaremos este por razones de simplicidad:

* [Buscar Categorías](../categories/category.md)

### Paso 2. Escoger una herramienta para hacer tu solicitud

Ciertas solicitudes pueden ser simples y directas, otras pueden requerir más experticia para hacer. Por eso en iTalento hemos trabajado en reducir al máximo la complejidad de las solicitudes.

A continuación expondremos algunas de las herramientas recomendadas y como usarlas:

#### Postman

Postman es una plataforma de API para crear y utilizar API. En palabras más simples, permite crear solicitudes para API's REST.

Recomendamos que leas de forma minuciosa la [Documentación de Postman](https://learning.postman.com/docs/introduction/overview/) para hacer un uso correcto de esta herramienta.

También en cada solicitud incluida en la documentación de la API de iTalento hemos añadido un ejemplo en Postman para facilitar su comprensión.

También existen aplicaciones alternativas a Postman como [Insomnia](https://insomnia.rest/).

#### Código

Si estás interesado en realizar la solicitud con código, hemos puesto código de ejemplo en **Javascript** (Proximamente más lenguajes) para cada uno de los puntos finales de la API.

Por ejemplo este es uno de los códigos que te vas a encontrar durante tu recorrido por la documentación, este código devuelve todas las categorias existentes en iTalento.

```js
fetch("https://italento.shop/categorias")
  .then((response) => response.json())
  .then((json) => console.log(json));
```

:::note[Nota]

Si tienes algún problema, consulta la `documentación para desarrolladores` del punto final al que estás realizando la solicitud o crea un issue en nuestro [GitHub](https://github.com/Kanto-Software-Solutions/iTalento-docs/issues) para obtener ayuda. Le ayudaremos a realizar la solicitud correctamente.

:::

### Paso 3. Revisa tu solicitud

Cuando hayas hecho una solicitud correctamente, recibirás un paquete con toda la metadata relacionada a la solicitud.

Si usas un punto que utiliza un método GET HTTP, recibiras datos relacionados al recurso (Publicación, Usuario, Categoria, etc) al que le hiciste la solicitud en formato JSON. Revisa los diferentes campos que retornaron y relaciona la información recibida con la del contenido en iTalento.

Si has utilizado un punto final que utiliza un método HTTP POST, PUT o DELETE, has realizado una acción en iTalento. Visita italento.shop o realiza una solicitud GET y comprueba si puedes rastrear esa acción.

### Paso 4. Ajusta tu solicitud con parámetros

Cada punto tiene un diferente conjunto de parámetros que puedes usar para alterar tu solicitud. Por ejemplo, puedes solicitar los datos de diferentes usuarios o de un único usuario al cambiar el campo de id en la solicitud GET. Puedes experimentar con diferentes funciones como [buscar Publicaciones], [buscar publicaciones por usuario] para filtrar los datos que realmente necesitas.

### Recursos Adicionales

* [Métodos HTTP](https://developer.mozilla.org/es/docs/Web/HTTP/Methods)
* [Solicitudes en Postman](https://learning.postman.com/docs/sending-requests/requests/)