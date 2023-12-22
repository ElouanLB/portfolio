<template>
<div class="app" ref="app">

<!-- Appel des composants "Header" et "Footer" pour qu'ils soient dans toutes les pages. RouterView pour la page en cours. -->

<Header />
<Router-View ref="routerView"/>
<Footer />
</div>
</template>

<script>
import { RouterView } from 'vue-router'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components:{
    Header,
    Footer,
  },
}
</script>



<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,400;0,700;0,900;1,400&family=Quicksand:wght@400;500;700&display=swap');

.app{
  width: 100%;
}
</style>