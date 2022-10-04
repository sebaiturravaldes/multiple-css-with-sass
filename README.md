# Múltiples CSS de salida con SASS usando node-sass

Para generar múltiples archivos de salida .css usando node-sass, es necesario indicarlo con el siguiente script 

```js
...
    "build-css": "node-sass --include-path scss scss/ --output css/",
...
```

## Primer requisito
No especificar un archivo de entrada y salida, solo los directorios, y antes del directorio de salida, agregar el parámetro `--output`

Con eso ya estamos listo con el primer requisito.

## Segundo requisito
El segundo requisito es que en tu carpeta de entrada, donde tienes tus archivos [.scss|.sass], los archivos que no quieras incluir en las salidas del CSS, deben comenzar con el `_` (guión bajo)

Por ejemplo, si quieres excluir un archivo de su salida quedaría algo como: `scss/_button.scss`
