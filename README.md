# reddit_api

> A Vue.js project
![alt text](https://liuji-jim.gallerycdn.vsassets.io/extensions/liuji-jim/vue/0.1.5/1478501659069/Microsoft.VisualStudio.Services.Icons.Default)

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

(Español)

Este es un pequeño proyecto realizado en un dia, aunando Vue 2.0 y Materialize para crear una app que comsume servicios API de reddit.

(English)

This is a little project created in one day, working with Vue 2.0 and Materialize to build an app that uses API services from reddit public API

![alt text](https://user-images.githubusercontent.com/40801686/42336415-e8be5cae-8083-11e8-8b9e-23367206ebdb.png)

(Español)

En dicho proyecto se han abordado conceptos como condicionales, bucles, eventos, text interpolation, v-bind, Conexiones remotas con Axios, creacion de components Vue etc. He decidido obviar elementos como vue-router o lifecycle-hooks, en cualquier caso serian integrados una vez siga con el proyecto.

Para la generacion del proyecto usé Vue CLI asi como node para levantar un servidor local. El proyecto integra webpack para el bundle de archivos. 

(English)

On this project I have used concepts like conditionals, loops, events, text interpolation, v-bind, remote connections with Axios, vue Components etc. I have decided to ignore elements like vue-router or lifecycle-hooks, but in any case it would be integrated once I decide to continue the project again.

To craft this project I installed the Vue CLI as well as Node to rise a local server. This project comes with webpack to bundle all the necessary files.


## INFORMACION BASICA DE LA APLICACION - Basic Information of the application

(Español)

Dicha app consiste en un buscador HTML que mediante evento keyup llama a una funcion Vue y conecta mediante axios con una API publica de reddit.

(English)

This app consists in a HTML search engine that have attached a keyup event and basically calls a Vue function that connects via Axios with the public reddit API


![alt text](https://user-images.githubusercontent.com/40801686/42336419-e9d5aa70-8083-11e8-91c0-c9010f125e72.png)

