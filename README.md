# Maquetus boilerplate

Boilerplate destinado a generar el HTML, CSS, JS y los assets asociados para entregar una maquetación web.

## Características

- [Handlebars](https://handlebarsjs.com/) mediante [Maquetus](https://github.com/javipuche/maquetus) para el HTML.
- Estilos mediante [Sass](https://sass-lang.com/) pasándole [Autoprefixer](https://github.com/postcss/autoprefixer).
- Transpila el Javascript mediante [Babel](https://babeljs.io/).
- Minifica CSS y el JS.
- Optimización de imágenes.
- Lanza un servidor local para el desarrollo.
- Refresco automático del navegador al detectar un cambio.

## Requisitos

- [Node.js](https://nodejs.org/en/)
- [Gulp.js](https://gulpjs.com/)

## Descarga

1. Descargamos `git clone https://github.com/javipuche/maquetus-boilerplate.git`.
2. Entramos en el proyecto `cd maquetus-boilerplate`.
3. Instalamos dependencias `npm install`.

## Uso

- Modo desarrollo: `npm run dev`.
- Modo producción: `npm run build`.

## Estructura de archivos

```
.
├── ...
├── builder       
├── dist       
├── src       
│   ├── assets   
│       ├── fonts   
|           └── ...   
│       ├── images   
|           └── ...   
│       ├── js   
│           ├── app   
│               ├── app.js   
|               └── ...   
|           └── ...   
│       ├── sass   
│           ├── app   
│               ├── example
│                   ├── example.scss  
|                   └── ...     
│               ├── styles.scss   
|               └── ...   
|           └── ...   
|       └── ...   
│   ├── components   
│       ├── example-component  
│           ├── example-component.config.json
│           ├── example-component.data.json  
│           ├── example-component.hbs
│           ├── example-component.md
|           └── ...  
|       └── ...   
│   ├── data   
|       └── ...   
│   ├── helpers  
|       └── ...
│   ├── layouts    
|       ├── default.hbs         
|       └── ...
│   ├── pages    
|       ├── home.hbs        
|       └── ...
│   └── partials       
|       └── ...     
└── ...
```

### Directorios

**IMPORTANTE:** Será necesario reiniciar el servidor al crear, mover o borrar un archivo en los directorios `sass/app` y `js/app`, ya que son entradas en la configuración de webpack.

| Directorio   | Descripción                                                                                                                                                                                                             |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `dist`       | Si estás en modo desarrollo sólo contendrá la carpeta `docs/components`, todo lo demás se carga en memoria. En modo producción contendrá el compilado final con todos los entregables y desaparecerá la carpeta `docs`. |
| `src`        | Contiene todos los archivos del proyecto.                                                                                                                                                                               |
| `assets`     | Contiene todos los assets del proyecto, como fuente, imágenes, estilos, javascript, etc.                                                                                                                                |
| `fonts`      | Contiene todas las fuentes del proyecto.                                                                                                                                                                                |
| `images`     | Contiene todas las imágenes del proyecto.                                                                                                                                                                               |
| `js`         | Contiene todo el javascript. Sólo los archivos  que estén en la carpeta `app` se transpilarán dentro de `dist/asses/js`. Ej: `dist/asses/js/app.js` para lo común y `dist/asses/js/custom.js` para algo concreto.       |
| `sass`       | Contiene todos los estilos. Sólo los archivos  que estén en la carpeta `app` se compilarán dentro de `dist/asses/css`. Ej: `dist/asses/js/styles.css` para lo común y `dist/asses/js/custom.css` para algo concreto.    |
| `components` | Contiene todos los components en Handlebars.                                                                                                                                                                            |
| `data`       | Contiene todos los modelos en `json` o `yml`. Más info en [Maquetus](https://github.com/javipuche/maquetus).                                                                                                            |
| `helpers`    | Contiene todos los `helpers`. Más info en [Maquetus](https://github.com/javipuche/maquetus).                                                                                                                            |
| `layouts`    | Contiene todos los `layouts`. Más info en [Maquetus](https://github.com/javipuche/maquetus).                                                                                                                            |
| `pages`      | Contiene todas las `pages`. Más info en [Maquetus](https://github.com/javipuche/maquetus).                                                                                                                              |
| `partials`   | Contiene todos los `partials`. Más info en [Maquetus](https://github.com/javipuche/maquetus).                                                                                                                           |
