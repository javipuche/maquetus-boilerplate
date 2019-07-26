---
pageTitle: 'Documentación'
---

# Introducción

Todos los archivos referentes a la documentación y/o configuración están en `src/docs`.

<hr>

## Configuración

Dentro de `src/docs` podremos encontrar un archivo llamado `config.json` donde van las diferentes opciones.

### Opciones

| Opción           | Tipo     | Descripción                                                                                                        |
| ---------------- | -------- | ------------------------------------------------------------------------------------------------------------------ |
| `previewStyles`  | `Array`  | Array de enlaces a estilos que se incluirán dentro de la vista previa del componente. Ej: `/assets/css/styles.css` |
| `previewScripts` | `Array`  | Array de enlaces a scripts que se incluirán dentro de la vista previa del componente. Ej: `/assets/js/app.js`      |
| `navigation`     | `Object` | Ordena los elementos de la navegación.                                                                             |

<hr>

## Páginas

Todas las páginas de la documentación están en markdown, ej: `example.md`. Puedes encontrar más info de como usar markdown en [este enlace](https://daringfireball.net/projects/markdown/syntax).

### Opciones de página

De manera opcional puedes pasar una serie de parámetros en cada una de las páginas para la configuración de la siguiente manera:

```yaml
---
pageTitle: 'Lorem ipsum dolor sit amet'
---

Lorem ipsum dolor sit amet, consectetur adipisicing elit. Maxime, illum!
```

#### Opciones

| Opción      | Tipo     | Descripción                                                   |
| ----------- | -------- | ------------------------------------------------------------- |
| `pageTitle` | `String` | Título del documento y título que aparecerá en la navegación. |

### Separar secciones

Automáticamente antes de cada `h2` se hace una separación para facilitar la lectura. Pero también puedes hacer una manual usando `<hr>`.

## Navegación

La navegación se genera automáticamente siguiendo los siguientes patrones:

- Por cada página existente en la documentación crea un grupo de enlaces.
- El título de dicho grupo se pasa por parámetro en la página mediante `pageTitle`, en caso de no existir usará el nombre del archivo.
- Cada enlace se genera a partir de cada encabezado de la página siguiendo su jerarquía.

### Ordenar la navegación

Por defecto el orden de la navegación será el de lectura de las páginas. Sin embargo puedes ordenarla en el archivo `src/docs/config.json` mediante el parámetro `navigation`:

```json
{
    "navigation": {
        "documentacion": 1,
        "botones": 2
    }
}
```

Para ordenar basta con pasar como `key` el nombre del `pageTitle` o el nombre del archivo en caso de no tener un `pageTitle` con los siguientes requisitos:

- Todo minúsculas.
- Cambiar espacios por guiones medios.
- Sin acentos.
- Cambiar `ñ` por `n`.

## Usar un componente

Para usar un componente en la documentación bastará con escribir:

```plaintext
@preview(example-component/example-component)
```
