<template>

  <!-- <HolaMundoView></HolaMundoView> -->
  <!-- <ContadorView/> -->
  <!-- <EstudianteView/> -->
  <!--EstudianteTablaViewVue/>-->
  <!-- <BibliotecaView /> -->
  <PreguntaView />


</template>

<script>
import HolaMundoView from "@/views/HolaMundoViews.vue";
import ContadorView from "@/views/ContadorView.vue"
import EstudianteView from "@/views/EstudianteView.vue"
import EstudianteTablaViewVue from "@/views/EstudianteTablaView.vue"
import BibliotecaView from "@/views/BibliotecaView.vue";
import PreguntaView from './views/PreguntaView.vue';


export default {
  name: 'App',
  components: {
    HolaMundoView,
    ContadorView,
    EstudianteView,
    EstudianteTablaViewVue,
    BibliotecaView,
    PreguntaView,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
