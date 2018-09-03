# Sitio web de elComité


## Instalación

Se requiere [tener instalado yarn](https://yarnpkg.com/en/docs/install) en el equipo para instalar el proyecto.  
Tras instalar yarn, en el directorio del proyecto, ejecutar este comando:

```bash
yarn install
```

## Levantar entorno de pruebas/desarrollo

Mediante el siguiente comando, tendremos levantado el sitio web en http://localhost:8080  
```bash
yarn docs:dev
```

## Generar el código del sitio estático

Mediante el siguiente comando, se generará todo el código en un directorio /www.  
Este código se podrá subir a cualquier servidor web capaz de servir html.  
```bash
yarn docs:build
```


