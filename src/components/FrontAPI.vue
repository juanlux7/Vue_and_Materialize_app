<template>
  <div>

  <div id="index-banner" class="parallax-container">
    <div class="section no-pad-bot">
      <div class="container">
        <div class="alert" v-if="errorMsg">
        <span class="closebtn" onclick="this.parentElement.style.display='none';">&times;</span>
            {{ errorMsg }}
        </div> 
        <br><br>
        <h1 class="header center teal-text text-lighten-2">Reddit API search</h1>
        <div class="row center">
          <h5 class="header col s12 light">A modern responsive front-end framework based on Material Design</h5>
        </div>
        <div class="row center">
           <input name="category" v-model="category" placeholder="select a category" id="category" type="text" class="validate" v-on:keyup="getCategory($event)">
          <label for="category">Search in Reddit (sports, videogames, memes...)</label>
        </div>
        <br><br>

      </div>
    </div>
    <div class="parallax"><img src="../../static/images/background1.jpg" alt="Unsplashed background img 1"></div>
  </div>

  

    <h2 v-if="dataSearch && !errorMsg">category selected: {{ category }}</h2>

    <div class="row">
    <div class="col s4 m4" v-for="el in elementos" :key="el.data.title">
      <div class="card" v-if="el">
        <div class="card-image">
          <div v-if="el.data.thumbnail != ''">
                <img v-bind:src="el.data.thumbnail" alt="el.data.title">
            </div>

          <div v-else>
                <p>there is no image available</p>
            </div>

          <span class="card-title">{{ el.data.title }}</span>


        </div>
        <div class="card-content">
          <p>get more about this: <a v-bind:href="el.data.url" target="_blank">here</a></p>
        </div>
        <div class="card-action">
          <p>likes: {{ el.data.score}}</p>
        </div>
      </div>
    </div>
    </div>

  <div class="container">
    <div class="section">

      <div class="row">
        <div class="col s12 m4">
          <div class="icon-block">
            <h2 class="center brown-text"><i class="material-icons">Vue technology</i></h2>
            <h5 class="center">Speeds up development with this great JS library</h5>

            <p class="light">Using Vue, you can perform powerfull task with less lines of code (this is better than a lorem ipsum paragraph LOL)</p>
          </div>
        </div>

        <div class="col s12 m4">
          <div class="icon-block">
            <h2 class="center brown-text"><i class="material-icons">group</i></h2>
            <h5 class="center">User Experience Focused</h5>

            <p class="light">By utilizing Vue and principles of Material Design, we were able to create a framework that incorporates components and animations that provide more feedback to users. Additionally, a single underlying responsive system across all platforms allow for a more unified user experience.</p>
          </div>
        </div>

        <div class="col s12 m4">
          <div class="icon-block">
            <h2 class="center brown-text"><i class="material-icons">settings</i></h2>
            <h5 class="center">Easy to work with</h5>

            <p class="light">Just using Vue and Materialize, you can build very interesting things from scratch. Esta es una descripcion de lo maravilloso de esta libreria (another lorem ipsum ommited)</p>
          </div>
        </div>
      </div>

    </div>
  </div>


  

  <div class="container">
    <div class="section">

      <div class="row">
        <div class="col s12 center">
          <h3><i class="mdi-content-send brown-text"></i></h3>
          <h4>Contact Me</h4>
          <p class="left-align light">Hello I am a junior programmer, my name is Juan and I am from Spain. I really enjoy learning new languages and I want to become a developer someday. Please write to my contact email if you have questions about anything. Thanks for watching</p>
          <hr>
          <p class="left-align light">Hola soy un programador junior llamado Juan y soy de España. Realmente disfruto aprendiendo nuevos lenguajes y me gustaria convertirme en programador algun dia. Por favor, escribeme a mi mail si tienes alguna cuestion sobre cualquier asunto. Gracias por verme</p>
        </div>
      </div>

    </div>
  </div>


  <div class="parallax-container valign-wrapper">
    <div class="section no-pad-bot">
      <div class="container">
        <div class="row center">
          <h5 class="header col s12 light">A modern responsive front-end framework based on Material Design</h5>
        </div>
      </div>
    </div>
    <div class="parallax"><img src="../../static/images/background3.jpg" alt="Unsplashed background img 3"></div>
  </div>

  <footer class="page-footer teal">
    <div class="container">
      <div class="row">
        <div class="col l6 s12">
          <h5 class="white-text">My Bio</h5>
          <p class="grey-text text-lighten-4">Soy un estudiante de FP que ama la programacion. Intento aprender por cuenta propia las ultimas tecnologias de lenguajes como Javascript, PHP, JAVA, C# etc. Me dedico a la programacion por hobby y me gusta aprender mediante proyectos open source en ingles y español.</p>


        </div>
        <div class="col l3 s12">
          <h5 class="white-text">Settings</h5>
          <ul>
            <li><a class="white-text" href="#!">Link 1</a></li>
            <li><a class="white-text" href="#!">Link 2</a></li>
            <li><a class="white-text" href="#!">Link 3</a></li>
            <li><a class="white-text" href="#!">Link 4</a></li>
          </ul>
        </div>
        <div class="col l3 s12">
          <h5 class="white-text">Connect</h5>
          <ul>
            <li><a class="white-text" href="https://github.com/juanlux7" target="_blank">GitHub</a></li>
            <li><a class="white-text" href="https://facebook.com/juanlunalama" target="_blank">Facebook</a></li>
            <li><a class="white-text" href="" target="_blank">Linkedin</a></li>
            <li><a class="white-text" href="#!" target="_blank">Twitter</a></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="footer-copyright">
      <div class="container">
      Made by <a class="brown-text text-lighten-3" href="http://materializecss.com">Materialize</a>
      </div>
    </div>
  </footer>


  </div>
</template>

<script>

import axios from 'axios';

export default {


  name: 'FrontAPI',
  data: function () {
        return {
            category: "",
            urlBase: "https://www.reddit.com/r/all/top.json?limit=10",
            elementos: [],
            dataSearch: false,
            limit: 10,
            errorMsg:''
            }
        },
    methods: {
        // defino el metodo que se encarga de conectar con la API mediante AXIOS
        getCategory(event){ 
            if(event.keyCode == 13){
                //console.log(this.category);
                axios.get("https://www.reddit.com/r/"+this.category+"/top.json?limit="+this.limit).then(
                    response => {
                        this.elementos = response.data.data.children;
                        this.errorMsg = "";
                    }
                ).catch(e => {
                    this.errorMsg = "there is no results for: "+this.category
                });
            }
        }
    }
}
</script>
