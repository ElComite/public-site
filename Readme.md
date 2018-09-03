# Sitio web de elComité


## Instalación

Se requiere [tener instalado yarn](https://yarnpkg.com/en/docs/install) en el equipo para instalar el proyecto.  
Tras instalar yarn, en el directorio del proyecto, ejecutar este comando:

```bash
yarn install
```

## Crear contenido

El contenido del sitio se guarda en archivos markdown dentro del directorio docs.  

Si añadimos un archivo llamado prueba.md, podremos verlo publicado como /prueba.html.  

## Levantar entorno de pruebas/desarrollo

Mediante el siguiente comando, tendremos levantado el sitio web en http://localhost:8080  
```bash
yarn docs:dev
```

## Generar el código del sitio estático

Mediante el siguiente comando, se generará todo el código en un directorio llamado www en la raíz del proyecto.  
El contenido de ese directorio es en sí todo el sitio web que se podrá subir a cualquier servidor web capaz de servir html.  
```bash
yarn docs:build
```


