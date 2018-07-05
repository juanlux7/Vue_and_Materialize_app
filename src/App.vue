<template>
  <div id="app">
    <NavBar/>
    <FrontAPI/>
  </div>
</template>

<script>

// importando componentes de la app, para registrarlos

import FrontAPI from './components/FrontAPI'
import NavBar from './components/NavBar'

export default {
  name: 'App',
  components: {
    FrontAPI,
    NavBar
  }
}
</script>

<style>

</style>
