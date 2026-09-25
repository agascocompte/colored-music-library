# Colored Music Library

Biblioteca musical compartida por [Colored Music](https://agascocompte.github.io/colored-music/) y [Colored Music Astra](https://agascocompte.github.io/colored-music-astra/).

Este es el único repositorio donde se mantienen las canciones. Las dos aplicaciones leen [library.json](https://agascocompte.github.io/colored-music-library/library.json) y reproducen los archivos de esta biblioteca.

## Añadir una canción

1. Sube el archivo a la carpeta `sounds/` de **este repositorio**.
2. Añade una entrada al array `tracks` de `library.json`:

```json
{
  "id": "mi-cancion",
  "title": "Mi canción",
  "artist": "Nombre del artista",
  "url": "sounds/MiCancion.mp3"
}
```

El `id` debe ser único, `artist` es opcional y la ruta debe coincidir exactamente con el archivo, incluidas mayúsculas y minúsculas. Separa las entradas con comas y conserva JSON válido.

3. Guarda los cambios en `main`. Cuando termine el despliegue de GitHub Pages, recarga las aplicaciones. No es necesario modificar ni desplegar los repositorios de los visualizadores.

## Quitar una canción

Elimina su entrada de `library.json`. También puedes eliminar su archivo de `sounds/` si ya no lo necesitas. Publica los cambios y recarga las webs.

## Publicación

GitHub Pages publica la raíz de la rama `main`. `.nojekyll` permite servir los archivos directamente. Las rutas del catálogo son relativas a su URL, por lo que las dos aplicaciones resuelven las canciones desde este repositorio.

Los archivos cargados localmente y los fragmentos del buscador de las aplicaciones solo duran esa sesión; no se añaden automáticamente a esta biblioteca.
