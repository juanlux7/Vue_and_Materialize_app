# reddit_api

> A Vue.js project ![alt text](https://liuji-jim.gallerycdn.vsassets.io/extensions/liuji-jim/vue/0.1.5/1478501659069/Microsoft.VisualStudio.Services.Icons.Default)

## Build Setup (instrucciones de ejecucion)

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run e2e tests
npm run e2e

# run all tests
npm test
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
# Vue_and_Materialize_app

Este es un pequeño proyecto realizado en un dia, aunando Vue 2.0 y Materialize para crear una app que comsume servicios API de reddit.

![alt text](https://user-images.githubusercontent.com/40801686/42336415-e8be5cae-8083-11e8-8b9e-23367206ebdb.png)

En dicho proyecto se han abordado conceptos como condicionales, bucles, eventos, text interpolation, v-bind, Conexiones remotas con Axios, creacion de components Vue etc. He decidido obviar elementos como vue-router o lifecycle-hooks, en cualquier caso serian integrados una vez siga con el proyecto.

Para la generacion del proyecto usé Vue CLI asi como node para levantar un servidor local. El proyecto integra webpack para el bundle de archivos. 

## INFORMACION BASICA DE LA APLICACION

Dicha app consiste en un buscador HTML que mediante evento keyup llama a una funcion Vue y conecta mediante axios con una API publica de reddit.


![alt text](https://user-images.githubusercontent.com/40801686/42336419-e9d5aa70-8083-11e8-91c0-c9010f125e72.png)

